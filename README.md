# CS 160 Concurrent Programming and Parallel Systems

## Introduction

**Description**: CS 160 is a project-driven course in which topics in concurrent programming and parallel systems are introduced through a quarter-long project. The project consists of multiple phases, which can also be viewed as a sequence of incremental projects—each building on the previous one and introducing more advanced features. The goal of this project is to motivate students to learn the importance of relevant topics and get hands-on experience with necessary design and development skills.

**Project Theme**: The theme of this project is a high-performance graph system that supports multiple advanced features that involve parallel and concurrent operations. It also involves the discussion of data locality and redundancy, two critical aspects for optimizing the performance of parallel systems.

**Language**: All phases must be implemented in C++.

**Team Size**: By default, students form teams of two students ([signup link](https://docs.google.com/spreadsheets/d/10G69h_2ubFoPdIM9VCHTI6BzP_dc70Qin4SSKubjH-w/edit?gid=0#gid=0)). However, if you have a strong desire to work individually on these projects, feel free to let the TA know. 

**Evaluation Criteria**: The phase of this project is evaluated based on the follow criteria:

- *Correctness* (50% per team): The TA will evaluate the correctness of the system using a set of test cases. Initially, a subset of these test cases will be released to students. Students then develop their own test cases to more thoroughly verify the correctness of their systems.

- *Performance* (20% per team): Performance is a primary goal in developing parallel systems. Our evaluation will assess whether the system achieves the expected level of performance. Note that expectations are relative to the hardware used—for example, one student may have a 4-core laptop, while another has a 16-core desktop. Students are encouraged to consult the TA in advance if they are unsure about the performance expectations.  
    
- *Development journal* (20% per student) \+ *Git commits* (10% per student): Students are required to document their development process in a structured development journal (**template** available [here](DEVELOPMENT_JOURNAL_TEMPLATE.md)). The journal is intended to help track progress and encourage a systematic approach to problem solving. In addition, students are expected to follow agile development practices by making frequent, meaningful Git commits. Finally, students should *report and analyze the experimental results* at the end of each phase. 

**Grades Distribution**:

| Phase (Tentative) | Weeks | Point Percentage |
| :---- | :---- | :---- |
| Phase 1: Concurrent Local Queries | Week 2–3 | 8% |
| Phase 2a: Parallel Global Queries | Week 3–4 | 8% |
| Phase 2b: Push-based Graph Algorithms | Week 4-5 | 8% |
| Phase 2c: Lock-free Push and Sparse Worklists | Week 5-6 | 8% \+ 3% |
| Phase 3: Graph Update | Week 6–7 | 8% \+ 3% |
| Phase 4: Concurrent Update and Query | Week 7–9 | 8% \+ 3% |

**Due Date Rule**: The exact due date depends on your lab section. If you are in a Tuesday lab section, each phase is due the following Tuesday at 11:59 PM. If you are in a Thursday lab section, each phase is due the following Thursday at 11:59 PM.

**Late Submission Policy**:   
Each team can request a 3-day extension twice without penalty. However, the following due dates *remain in place*. No further extensions will be granted after that.

## Submission Instructions

For each phase, students will join an assignment using a link shared by the TA (in the eLearn announcement). After joining the assignment, students will receive an empty repository (team members share this repository). Students are expected to submit their code and development journal to this repository. The final submission for each phase should be made by the due date and will be used for grading.

Please organize the repository as follows:

```
├── code/                 # source code for this phase
├── journal/              # development journal for this phase
│   └── alex_session1.md  # each session is documented in a separate markdown/PDF file
│   └── jane_session1.pdf
```

Students are expected to include detailed experiments and analysis in their development journal. The TA will grade correctness and performance based on the experimental results and analysis reported in the journal, as well as the code submitted to the repository.