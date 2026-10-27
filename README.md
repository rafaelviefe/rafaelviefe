I'm Rafael, a backend software engineer in Florianópolis, Brazil (UTC-3). I build Java and Kotlin services for systems where latency and uptime matter.

At FITec I work on event-driven microservices for the provisioning and billing platform of a global telecom vendor: about 20 services on AWS EKS, ~5M events a day, a 99.99% SLA. Before that I worked on e-SUS APS, the electronic health record of Brazil's Ministry of Health, used in 26,000+ primary-care units.

A few things from that work:

- Took a subscriber API's p99 latency from 850 ms to 120 ms by re-keying Cassandra partitions (dual-write migration of 4 TB) and adding a Redis cache.
- Built the team's MCP server in Java with Spring AI. It gives AI agents read-only, audited access to orders, logs, metrics and deploys; 30+ engineers use it, and median incident triage dropped from 40 to 10 minutes.
- Found why an aggregation query on multi-TB PostgreSQL tables took a minute (a correlated EXISTS subquery running once per row) and got it under one second.

That code is private. What's public here:

- **[payment-intermediary](https://github.com/rafaelviefe/payment-intermediary)**: my Rinha de Backend 2025 entry. A Go load balancer, two Java 21 / Spring WebFlux instances on virtual threads compiled with GraalVM, and Redis queues with Lua scripts, sustaining 850 req/s with the whole stack capped at 1.5 vCPU and 350 MB of RAM.
- **[marcacao-mercado-calc](https://github.com/rafaelviefe/marcacao-mercado-calc)**: an open-source fixed-income calculator in TypeScript and Next.js. AUVP, one of Brazil's largest investing schools, adopted the code as the base of its own calculator.
- **[FlexPomodoro](https://flexpomodoro.vercel.app)**: a focus timer I built and run, with 1,000+ registered users.

Day to day: Java 21, Kotlin, Spring Boot, Apache Kafka, RabbitMQ, PostgreSQL, Cassandra, Redis, AWS, Kubernetes, Prometheus, Grafana, OpenTelemetry.

[LinkedIn](https://www.linkedin.com/in/rafael-vieira-ferreira) · rafaelviefe@gmail.com
