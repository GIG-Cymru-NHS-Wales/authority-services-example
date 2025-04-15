# Authority services example

This page describes an authority services example software product. This is
intended for discussion purposes, such as talking with our software engineering
teams about how they could try this kind of example, and what they might expect.

## Context example

Broadly, some of our medical clinicians and their departments need authority
services, meaning processes that says "yes" or "no" to questions such as "can I
do this?" or "can I see this?".

Some of these authority services are for clinicians with regard to internal
services, such as the authority to order various kinds tests, regardless of
patient. For example, a junior doctor may have authority to order a simple test,
whereas a senior doctor may have authority to order a complex test.

## Specific example

Specifically, our health board radiology departments need a way to specify which
clinicians have authority to order which kinds of radiology scans.

To the best of our knowledge, our current radiology vendor does not provide this
capability.

Our organization currently has some/all of the administrative data, such as the
clinician names, departments, and organizations, as well as the specific tests
and their codes.

To the best of our knowledge, our current setup doesn't have a self-service
authority service for this, such as a web app or web form or a web API, that
enables a radiology department to specify which clinicians have authority to
order which kinds of scans.

## Use case example

Use case sketch for the day-to-day path:

* I'm a radiologist.
  
* I want to know if I have authority to order a particular test.

* I can sign in to a web page, and see which tests I can order.

* Ideally I have a simple way to search for a particular test.

Use case sketch for the manager path:

* I'm a radiologist manager.
  
* I want to specify which of my radiologists have authority to order which tests.

* I can sign in to a web page, and associate my radiologists with my tests.

* Ideally I have a simple way to search my radiologists and my tests.

* Ideally I can create defaults, such as "all my radiologists can order this test".

## Pathway example

A pathway from idea to implementation could try these three steps:

1. Public prototype. This means building a public open source prototype that
   leverages all synthetic data, for the purpose of showing to the
   chain-of-command. This prototype would be a proof-of-product-concept. This is
   a new way of working for our software engineering because it aims to get
   working software into the hands of the users as fast as possible.

2. Protected discovery. This means researching what data we currently have about
   clinicians and tests, which specific clinicians are stakeholders (we believe
   there are 30 or so), and how to engage with them with real data (still no
   patient data). This is a new way of working for our software engineering
   because we'll introduce queueing theory (e.g. DORA metrics), test driven
   development with automatic tests, and continuous integration, continuous
   delivery, and continuous telemetry.

3. Production deployment. This launches the real product to the clinicians. This
   also verifies that production deployment works. This will involve a new way
   of working because we will deliberately use DORA metrics with resilience
   engineering, including deliberately shipping a bug and tracking what's
   involved in fixing it.
