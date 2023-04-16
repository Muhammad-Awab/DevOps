
### Continuous Integration

- Continuous Integration (CI) is a software development practice in which developers integrate code changes into a shared repository frequently, usually multiple times a day. 
- Each integration is then verified by an automated build and testing process to detect errors and conflicts as early as possible.
- The *goal of CI* is to ensure that all changes made to the codebase are tested and integrated with the main codebase in a timely manner, allowing for rapid feedback and detection of errors. 
- By catching issues early on, CI helps to reduce the time and effort required to fix problems and ensures that the codebase is always in a releasable state.
- CI is often used in conjunction with other software development practices such as *Continuous Delivery (CD) and Infrastructure as Code (IaC)* to support a **DevOps** approach to software development. 
- Together, these practices help to automate the software delivery process, ensuring that changes are tested, integrated, and deployed quickly and reliably.

#### Steps in CI

1. Developers **write and commit code** changes to a shared repository.
2. An **automated build process pulls** the changes and **compiles** the code.
3. **Automated tests are run** against the code to ensure that it meets the required quality standards.
4. If the **build or tests fail, the team is alerted** to the issue so that it can be addressed promptly.
5. If the **build and tests pass, the changes are merged** into the main codebase and the cycle continues.


 ### Continuous Delivery 

- Continuous Delivery (CD) is a software development practice in which software is built, tested, and deployed to production in a rapid and automated fashion. 
- The goal of CD is to enable software to be delivered to end-users quickly, with a high level of quality and reliability, while minimizing the risk of errors and downtime.
- In Continuous Delivery, the process of releasing software is automated, from the moment a code change is committed to a version control system to the moment it is deployed to production.
- CD enables teams to rapidly and reliably deliver software to end-users, with a focus on improving speed, quality, and reliability. 
- By automating the process of software delivery, CD helps to reduce the risk of errors, minimize downtime, and improve the overall user experience.
- CD is often used in conjunction with other software development practices, such as Continuous Integration (CI) and Infrastructure as Code (IaC), to support a DevOps approach to software development. 
- Together, these practices help to automate the software delivery process, ensuring that changes are tested, integrated, and deployed quickly and reliably.

<img src="../Images/continuous_delivery.png" style="zoom:120%;" />

#### Steps in CD

1. **Continuous Integration (CI**): Developers frequently integrate code changes into a shared repository, with each change verified by an automated build and testing process.
2. **Automated Testing**: Automated tests are run against the code changes to ensure that they meet the required quality standards.
3. **Continuous Deployment**: Code changes that pass testing are automatically deployed to a staging environment for further testing.
4. **Release Management**: Once the code changes have been thoroughly tested, they are released to production in a controlled and automated fashion.



<img src="../Images/continuous_integration.4f4cddb8556e2b1a0ca0872ace4d5fe2f68bbc58.png" style="zoom:120%;" />
