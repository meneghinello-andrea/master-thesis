# Master Thesis in Computer Science

In order to complete my MSc in Computer Science I choose, in agreement with my supervisor [Tullio Vardanega](tullio.vardanega@math.unipd.it), to analize nowadays leading technology in the Cloud Computing landscape.

---

#### Table of contents

* [Description](#markdown-header-description)
* [Phases](#markdown-header-phases)
* [Contents](#markdown-header-contents)
* [Compile the contents](#markdown-header-compile-the-contents)

---

### Description

Nowadays the virtualization technology is dominating the Cloud Computing landscape. Even if this technology is well consolidated and documented from many years of service in different field of computer science, it presents some limitations when it faces with **elasticity** and **scalability** that are common issues in Cloud Computing.

The purpouse of this study is to compare the **Docker Containers**, a [Linux Containers (LXC)](https://linuxcontainers.org) revisitation proposed by **[Docker company](https://www.docker.com)**, that promise to be a good technology to build **distribuited applications** deployable in Cloud Environments.

Docker asserts that using its containers instead classic Virtual Machines, managed by an hypervisor, as foundations in new software architectures can lead developers to build **more easily scalable** and **multi-tenant** applications that can **exploit better** the Cloud Computing capabilities.

---

### Phases

My work started with a depth study in **Docker Containers Architecture** in order to understand the work made, by Docker company, in the following field:

* processes isolation;
* File System isolation;
* security (data integrity, data consistency).

In a second phase I designed and executed some comparison tests in order to compare both technology in the three major axes that lead the Cloud Computing (**compute**, **storage**, **network**).

Finally, with the result obtained I designed a prototype of a software architecture to build a **scalable** and **multi-tenant** application that exploits Cloud Computing capabilites using the new features offered by Docker Containers.

---

### Contents

This reposity contains all the work done during my Master Thesis, and in particular you can find:

* a [LaTeX](https://www.latex-project.org) document that illustrates all the steps done;
* a [Latex](https://www.latex-project.org) Beamer presentation that I used to illustrate the work done to the commission;
* an Excel directory that contains the raw collected data and the plotted charts.

---

### Compile the contents

In order to obtain a readable PDF document, of both report and presentation, I provide [makefile](https://wn.wikipedia.org/wiki/Make_(software)) for both the documents.

To use it in a Unix based system simply place a bash shell in the directory that contains the desidered document and run one of the following commands (they have the same purpose):

* make
* make compile

To clean the environment simply place a bash shell in the directory where you have compiled the PDF document and run the following command:

* make clean

---