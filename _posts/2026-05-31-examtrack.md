---
title: "Working at ExamTrack"
date: 2026-05-31
layout: post
---

I have recently started a new job at ExamTrack, working with the development team
on a fairly large Ruby on Rails application. The platform is made up of several
Rails engines and has been around for some time, so part of the job is getting to
know the existing codebase while helping to modernise it.

My main area of responsibility is application security and DevOps. I have been
setting up a DevSecOps pipeline using tools including Brakeman for static analysis
and OWASP ZAP for dynamic scanning, alongside the usual CI/CD work and
containerised development environments.

That has proven to be a challenge in places. The application has more than 4,000
endpoints, with different workflows and connections to third-party services.
Some findings also need to be understood rather than blindly treated as bugs. For
example, ZAP reports a subresource integrity warning for Google's reCAPTCHA
JavaScript library. The script changes over time, so Google does not provide a
stable public hash that can be added to the application.

This has already turned up useful things to work on. One example was patching a
SQL injection issue inside the Rails application and making sure the same kind of
problem is easier to catch automatically in future. That is the main reason I
was asked to add the scanning tools to the pipeline: they are much more useful
when they are part of normal development rather than something run occasionally.

I am also contributing to the Rails code itself, tests, performance work and
documentation. It is a varied role, but it has been a good opportunity to put my
cyber security degree into practice while getting more experience with a large
existing application.
