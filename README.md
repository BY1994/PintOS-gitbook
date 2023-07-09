# 🌈 Pintos 에 오신 것을 환영합니다

[![](https://github.com/PKU-OS/Pintos-gitbook/raw/master/.gitbook/assets/pkuos.svg)](https://github.com/PKU-OS/Pintos-gitbook/blob/master/.gitbook/assets/pkuos.svg)

### 소개

**Pintos 는 80x86 아키텍처를 위한 간단한 운영체제 프레임워크입니다.** 이것은 **커널 스레드, 유저 프로그램을 로딩하고 실행하는 것**, 그리고 **파일 시스템**을 지원합니다. 하지만 이것은 이 모든 기능을 매우 간단한 방식으로 구현합니다. Pintos 프로젝트에서, 여러분은 이 기능들을 세 가지 영역으로 확장시킬 것입니다. 여러분은 또한 가상 메모리 구현을 추가할 것입니다.

**Pintos는 이론적으로는 통상적인 IBM 호환 PC 에서 동작할 수 있습니다.** 안타깝게도, Pintos 를 사용하기      위해 모든 학생들에게 할당된 PC 를 다 지원할 수는 없습니다. 그러므로, 우리는 Pintos 프로젝트를 시스템 시뮬레이터에서 돌릴 것입니다. 이 시뮬레이터는 80x86 CPU 와 주변 장치들을 가상으로 만든 것으로 운영체제나 소프트웨어를 수정 없이 실행할 수 있습니다. 수업에서 우리는 [Bochs](http://bochs.sourceforge.net/) 와 [QEMU](http://fabrice.bellard.free.fr/qemu/) 시뮬레이터를 사용할 것입니다. 또한  Pintos 는 [VMware Player](http://www.vmware.com/) 로도 테스트가 되었습니다.

**이 프로젝트는 어렵습니다.** 시간이 오래 걸리는 것으로 잘 알려져있고, 실제로도 그렇습니다. 저희는 작업 부담을 줄이기 위해 많은 지원 문서를 제공한다거나 하는 일들을 할 것입니다. 하지만 여전히 해야할 많은 어려운 일들이 있습니다. 저희는 여러분의 피드백을 환영합니다. 만일 불필요한 과제 부담을 줄일 수 있거나, 중복되는 작업에 주의가 분산되지 않도록 하거나, 학생들이 중요한 부분에만 집중할 수 있도록 하는 아이디어가 있으시다면, 저희에게 알려주시기 바랍니다.

### History

Pintos was originally developed at Stanford by Ben Pfaff [blp@cs.stanford.edu](mailto:blp@cs.stanford.edu) to substitute for the old OS course project Nachos. After more than a decade of iterations, Pintos has been adopted by over fifty institutes as the OS course project, including Stanford, UC Berkeley, Carnegie Mellon, Johns Hopkins, and so on. You can read the original [Pintos paper](https://benpfaff.org/papers/pintos.pdf) (Yes, they even write a paper for it !) to learn the details of Pintos' design philosophy and its comparison with other instructional operating system kernels, e.g., JOS, Nachos, GeekOS, and so on.

\{% hint style="info" %\} **Why the name "Pintos"?:**

First, like nachos, pinto beans are common Mexican food. Second, Pintos is small and a "pint" is a small amount. Third, like drivers of the eponymous car, students are likely to have trouble with blow-ups. —— Ben Pfaff \{% endhint %\}

### Project Overview

**There are five labs in total.** Lab0 is designed to prepare you for the later projects and practice your GDB ability, so it is intentionally much simpler than the remaining projects. In Lab1 - 4, you will extend Pintos in different dimensions and make it more robust and powerful.

| Project                       | Release   | Code Due           | Design Doc Due     | Content                                | Point |
| ----------------------------- | --------- | ------------------ | ------------------ | -------------------------------------- | ----- |
| **Lab0: Getting Real**        | **02/21** | **03/02 11:59 pm** | **03/05 11:59 pm** | Bootstrap Pintos                       | 4     |
| **Lab1: Threads**             | **03/07** | **03/23 11:59 pm** | **03/26 11:59 pm** | Kernel threads scheduling              | 9     |
| **Lab2: User Programs**       | **03/28** | **04/13 11:59 pm** | **04/16 11:59 pm** | Load & Run user programs, System calls | 9     |
| **Lab3a: Virtual Memory**     | **04/25** | **05/18 11:59 pm** | **05/21 11:59 pm** | Demand Paging                          | 9     |
| **Lab3b: Mmap Files**         | **05/23** | **06/01 11:59 pm** | **06/04 11:59 pm** | Mmap Files                             | 9     |
| (optional) Lab4: File Systems | **/**     | /                  | /                  | Implement File systems                 | 0     |

**In each lab, we will release all the test cases to support your local development.** After the deadline, we will run the same test suite to grade your submissions, so don't worry that your evil teaching assistants (TAs) will intentionally design many corner cases only to deduct your scores.

However, your evil TAs firmly believe that there is a great difference between "elegant code" and "working code". **So a large part of your score will be determined by the quality of your design document and your code.** Don't worry, your kind TAs firmly resist "involution" and advocates "Ockham's Razor", so we will provide document templates for you to limit your document to hundreds of words long. Also, we will make the scoring criteria of coding style publicly available.

**In a word, we hope this project will be a challenging but rewarding experience for all of you guys.** If you have any suggestions, feel free to contact PKUFlyingPig [zhongyinmin@pku.edu.cn](mailto:zhongyinmin@pku.edu.cn).

### Prerequisite

We highly recommend you read the [prerequisites](https://pku-minic.github.io/online-doc/#/preface/prerequisites) and [facing-problems](https://pku-minic.github.io/online-doc/#/preface/facing-problems) sections of the PKU Compiler Project.

### Version Control

We highly recommend you to use Git for version control in the class. If you are new to Git, there are plenty of tutorials online you can read, e.g., [this one](https://csdiy.wiki/%E5%BF%85%E5%AD%A6%E5%B7%A5%E5%85%B7/Git/).

### Submission

We will be using [PKU course website](https://course.pku.edu.cn/) to collect assignments and release your scores. See the submission section under each lab's description for more details.

**Pay attention to the deadline for each code and design doc submission.** Usually, the code submission dues three days earlier than its design doc submission (except for lab 0), which forces you to spend enough time to express your design ideas sufficiently but succinctly.

### Grading

**We will grade your assignments based on test results (60%) as well as design doc and code quality (40%).** Note that the testing grades are fully automated. So please turn in the working code, otherwise there is no credit (See section [Grading](https://github.com/PKU-OS/Pintos-gitbook/blob/master/getting-started/grading.md) for more details).

### Cheating and Collaboration

\{% hint style="danger" %\} **This class has zero tolerance for cheating.** We will run tools to check your submissions against a comprehensive database of solutions including past and present submissions for potential cheating. The stakes are very high. So do not cheat, do not cheat, do not cheat! \{% endhint %\}

**The basic policies for the project assignments are as follows:**

* **Never copy project code or text found on the Internet**, e.g., GitHub.
* **Never share code or text on the project.** That also means do not make your solutions public on the Internet.
* **Never use others' code or text in your solutions.** This includes code/text from prior years or other institutions.
* You may read but **not** copy Linux or BSD source code. **You must cite any document or code that inspired your code**. As long as you cite what you used, it's not cheating. In the worst case, we deduct points if it undermines the assignment.

**On the other hand, we encourage collaboration in the following form:**

* Explain a concept to another student, or ask another student to explain a concept to you.
* Discuss algorithms or approaches for an exercise. But you should not exchange, look at, or copy each other's code.
* Discuss testing strategies and approaches.
* Help someone else debug if they've got stuck. But you should not give that student code solution.

The course staff will actively detect possible ethics violations. For each project submission, **we will run automated cheating detection tools** to check your submission against a comprehensive database of solutions including solutions on the Internet, past submissions, and solutions from other institutions.

### What's next?

In the next chapter, you will set up your local development environment, boot Pintos and get familiar with its debugging and testing tools. You will use these utilities throughout the semester again and again and again. So read carefully and patiently \~\~

\
