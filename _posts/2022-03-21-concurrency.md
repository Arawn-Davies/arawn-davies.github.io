---
title: "Concurrency"
date: 2022-03-21
layout: post
---

I have recently been studying concurrent and parallel algorithms, including
semaphores, non-blocking algorithms, parallel threading and multitasking.

One exercise used a producer-consumer model: several chefs prepare cakes and place
them on a conveyor belt for customers. The conveyor is represented by an
infinite-size array, and each chef acts as a producer.

The original pseudo-code was:

```
while (true) {
    cake = makeCake();
    wait(empty);
    conveyor[in] = cake;
    in = (in + 1) mod n;
}
```

The `wait(empty)` operation does not fit an infinite buffer: unlike a bounded
buffer, there is no finite capacity that producers need to wait for. Multiple
producers still need synchronisation when updating the shared insertion index and
writing to the conveyor.

A revised version uses a mutex around that critical section and signals when a
new item is ready:

```
int in = 0;

while (true) {
    cake = makeCake();
    wait(producerMutex);
    conveyor[in] = cake;
    in++;
    signal(producerMutex);
    signal(ready);
}
```

This is a useful small example of the distinction between capacity control and
mutual exclusion. Removing an unnecessary wait does not remove the need to
protect shared state when several producers can update it concurrently.
