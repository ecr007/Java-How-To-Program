# Chapter 1

Souce codes: https://github.com/pdeitel/JavaHowToProgram10eEarlyObjectsVersion

Unit | Bytes | Approximately
--- | --- | ---
1 kilobyte (KB) | 1024 bytes | 10^3 (1024 bytes exactly)
1 megabyte (MB) | 1024 kilobytes | 10^6 (1,000,000 bytes)
1 gigabyte (GB) | 1024 megabytes | 10^9 (1,000,000,000 bytes)
1 terabyte (TB) | 1024 gigabytes | 10^12 (1,000,000,000,000 bytes)
1 petabyte (PB) | 1024 terabytes | 10^15 (1,000,000,000,000,000 bytes)
1 exabyte (EB) | 1024 petabytes | 10^18 (1,000,000,000,000,000,000 bytes)
1 zettabyte (ZB) | 1024 exabytes | 10^21 (1,000,000,000,000,000,000,000 bytes)

## 1.5.4 Reuse

<b>Software Engineering Observation 1.1</b>

Use a building block approach to creating your programs. Avoid reinventing the wheel use high quality pieces wherever possible. This Software reuse is a key benefit of object-oriented programming.

## 1.5.10 Object-Oriented Analysis and Design (OOAD)

To create the best solutions, you should follow a detailed analysis process for determining your project’s requirements (i.e., defining what the system is supposed to do) and developing a design that satisfies them (i.e., specifying how the system should do it). Ideally, you’d go through this process and carefully review the design (and have your design reviewed by other software professionals) before writing any code.

## 1.5.11 The UML (Unified Modeling Language)
Although many different OOAD processes exist, a single graphical language for communicating the results of any OOAD process has come into wide use. The Unified Modeling Language (UML) is now the most widely used graphical scheme for modeling object-oriented systems.

## 1.8

<b>Performance Tip 1.1</b>
Using Java API classes and methods instead of writing your own versions can improve program performance, because they’re carefully written to perform efficiently. This also shortens program development time.

https://docs.oracle.com/javase/8/docs/api/

## 1.9 A Typical Java Development Environment

<b>Step 1</b>: Create Java file with ```.java``` extension
<b>Step 2</b>: Compiling program with ```javac FILENAME.java```

The compile proccess produce ```.class``` files.

* JVM: Java Virtual Machine, its execute bytecodes 

<b>Step 3</b>: Run java programs ```java FILENAME```

## 1.12 Software Technologies

<b>Software as a Service (SaaS)</b>: the software runs on servers elsewhere on the Internet. When that server is updated, all clients worldwide see the new capabilities—no local installation is needed. You access the service through a browser. Browsers are quite portable, so you can run the same applications on a wide variety of computers from anywhere in the world. Salesforce.com, Google, and Microsoft’s Office Live and Windows Live all offer SaaS.

<b>Software Development Kit (SDK)</b>: include the tools and documentation developers use to program applications. For example, you’ll use the Java Development Kit (JDK) to build and run Java applications.

### Software Stage or Vesions

| Stage | Description |
| --- | --- |
| Alpha | Alpha software is the earliest release of a software product that’s still under active development. Alpha versions are often buggy, incomplete and unstable and are released to a relatively small number of developers for testing new features, getting early feedback, etc. |
| Beta | Beta versions are released to a larger number of developers later in the development process after most major bugs have been fixed and new features are nearly complete. Beta software is more stable, but still subject to change. |
| Release candidates | Release candidates are generally feature complete, (mostly) bug free and ready for use by the community, which provides a diverse testing environment—the software is used on different systems, with varying constraints and for a variety of purposes. |
| Final release | Any bugs that appear in the release candidate are corrected, and eventually the final product is released to the general public. Software companies often distribute incremental updates over the Internet. |
| Continuous beta | Software that’s developed using this approach (for example, Google search or Gmail) generally does not have version numbers. It’s hosted in the cloud (not installed on your computer) and is constantly evolving so that users always have the latest version. |
