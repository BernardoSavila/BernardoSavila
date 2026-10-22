<div align="center">

# Bernardo Ávila

**Backend developer** · Azores, Portugal
MSc student in Software Development and Interactive Systems

<a href="https://www.linkedin.com/in/bernardo-avila-dev"><img src="https://img.shields.io/badge/LinkedIn-2b3137?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:bernardosavila@gmail.com"><img src="https://img.shields.io/badge/Email-2b3137?style=flat-square&logo=maildotru&logoColor=white" alt="Email"></a>

</div>

<br>

I like the parts of backend work that only show up under load — the race condition that passes every manual test, the query that works until the table grows, the test that would pass whether or not the code was correct.

---

## Projects

### [slotly](https://github.com/BernardoSavila/slotly) — resource booking REST API

<img src="https://img.shields.io/badge/Java_25-2b3137?style=flat-square&logo=openjdk&logoColor=white" alt="Java 25"> <img src="https://img.shields.io/badge/Spring_Boot_4-2b3137?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot 4"> <img src="https://img.shields.io/badge/PostgreSQL-2b3137?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Testcontainers-2b3137?style=flat-square&logo=testcontainers&logoColor=white" alt="Testcontainers"> <img src="https://img.shields.io/badge/Docker-2b3137?style=flat-square&logo=docker&logoColor=white" alt="Docker">

The interesting part isn't the CRUD, it's the invariant: no two bookings for the same resource may overlap. The obvious check-then-insert is correct for one request at a time and wrong under load — two requests read an empty result in the same millisecond and both write. I fixed it with a pessimistic row lock on the resource, and verified it with a concurrency test that releases 10 threads onto the same slot against a real PostgreSQL in Testcontainers. The test fails when the lock is removed, which is the only kind of test worth having.

> [The README walks through the three strategies I weighed](https://github.com/BernardoSavila/slotly#preventing-overlapping-bookings) — `SERIALIZABLE` isolation, the pessimistic lock, and a GiST exclusion constraint — what each one costs, and what the current solution still doesn't protect against.

### [SportConnect](https://github.com/BernardoSavila/SportConnect) — sports team management

<img src="https://img.shields.io/badge/TypeScript-2b3137?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/Node.js-2b3137?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"> <img src="https://img.shields.io/badge/Express-2b3137?style=flat-square&logo=express&logoColor=white" alt="Express"> <img src="https://img.shields.io/badge/MySQL-2b3137?style=flat-square&logo=mysql&logoColor=white" alt="MySQL"> <img src="https://img.shields.io/badge/Flutter-2b3137?style=flat-square&logo=flutter&logoColor=white" alt="Flutter">

My final undergraduate project. REST API with JWT authentication and 60 automated tests across 12 suites, written alongside the API rather than after it. Flutter client, and the whole environment comes up with one Docker Compose command.

---

## Working with

<img src="https://img.shields.io/badge/Java-2b3137?style=flat-square&logo=openjdk&logoColor=white" alt="Java"> <img src="https://img.shields.io/badge/Spring_Boot-2b3137?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot"> <img src="https://img.shields.io/badge/Spring_Data_JPA-2b3137?style=flat-square&logo=spring&logoColor=white" alt="Spring Data JPA"> <img src="https://img.shields.io/badge/TypeScript-2b3137?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/Node.js-2b3137?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js">
<img src="https://img.shields.io/badge/PostgreSQL-2b3137?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/MySQL-2b3137?style=flat-square&logo=mysql&logoColor=white" alt="MySQL"> <img src="https://img.shields.io/badge/JUnit-2b3137?style=flat-square&logo=junit5&logoColor=white" alt="JUnit"> <img src="https://img.shields.io/badge/Testcontainers-2b3137?style=flat-square&logo=testcontainers&logoColor=white" alt="Testcontainers"> <img src="https://img.shields.io/badge/Docker-2b3137?style=flat-square&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/Maven-2b3137?style=flat-square&logo=apachemaven&logoColor=white" alt="Maven"> <img src="https://img.shields.io/badge/Git-2b3137?style=flat-square&logo=git&logoColor=white" alt="Git">

Currently learning Python, and putting LLM APIs into something that has to survive retries, streaming and a cost budget.

---

<div align="center">

Open to a first backend engineering role — Portugal, or remote for an EU or US team.

</div>
