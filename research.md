---
layout: page
title: Projects
---

## Leveraging Large Language Models for Automated Program Repair

<img src="../assets/img/bug.png"
alt="toga"
width="450"
height="220"
style="float: right;" />

This study explores the utility of Large Language Models (LLMs) in automated program repair (APR). Unlike prevailing deep learning-enabled APR methods, which typically address bug detection and resolution simultaneously, we argue for a distinct separation of these steps into multiple models. This approach facilitates enhanced integration of various types of contextual information and a flexible inclusion of inductive biases. Our proposed method outperforms existing approaches across various bug datasets, including Defects4J. Additionally, the paper explores numerous research questions, providing detailed discussions and answers, supported by thorough experimental analyses.

Details: Coming soon!

## Predictive Mutation Testing via Graph Transformer Network

Mutation testing, characterized by its resource-intensive nature—executing numerous mutants against extensive test suites—poses significant cost implications. In response to this challenge, this research introduces a prediction method founded on Graph Transformer Networks (GTNs), aiming to discern whether a test suite will detect a mutant without necessitating test suite execution. This method formulates a semantic graph derived from a system and its corresponding test suite, employing graph and mutant embeddings to predict mutant termination. Evaluated across various practical Java projects and a significant number of mutants, the method exhibits a marked reduction in test executions relative to conventional mutation testing, with only a slight trade-off in mutation score accuracy, and notably surpasses preceding Predictive Mutation Testing (PMT) methods in terms of accuracy

Details: Coming soon!

## Neural-Based Test Oracle Generation: A Large-scale Evaluation and Lessons Learned

<img src="../assets/img/toga.png"
     alt="toga"
     width="350"
     height="220"
     style="float: right;" />

Unlike automated test inputs generation, high-quality automated test oracle generation is comparatively less well solved by the software engineering community. Recently, neural-based test oracle generation techniques have shown promise in detecting real-world faults. However, these techniques generate too many false positive assertions that do more harm than good. In a large-scale study of 25 real-world Java systems, we evaluated a few recently published state-of-the-art machine learning and deep learning-based automated test oracle generation techniques. 

Details: [\[paper (FSE'23)\]](https://arxiv.org/pdf/2307.16023)


## Measuring and Mitigating Gaps in Structural Testing

<img src="../assets/img/icse23.png"
     alt="icse23"
     width="450"
     height="220"
     style="float: right;" />


Code coverage is used by millions of developers in thousands of organizations on a daily basis. Despite this popularity, code coverage has well-understood limitations demonstrated by the software engineering research community, such as not providing enough insight into test oracles' quality. In this research, we compute *coverage gaps*, a metric to detect the undertested program structures by analyzing the existing test oracles. We then propose a lightweight intra-procedural flow-insensitive static analysis technique that uses the system under test (SUT) and the coverage gaps as inputs to recommend actionable feedback to the developers to complement the test suite with additional test oracles, which demonstrated to improve the fault-detection effectiveness of the test suite.

Details: [\[paper (ICSE'23)\]](https://doi.org/10.6084/m9.figshare.21932058.v5) [\[artifact\]](https://github.com/soneyahossain/hcc-gap-recommender/tree/main) [\[talk\]]({{'/'|relative_url}}assets/presentations/ICSE-2023-talk.pdf) [\[poster\]]({{'/'|relative_url}}assets/presentations/ICSE2023_poster_soneya.pdf)


## MuSlicer: A Language Agnostic Dynamic Program Slicing Tool
	
<img src="../assets/img/slicer.png"
     alt="slicer"
     width="350"
     height="220"
     style="float: right;" />

Dynamic dependency analysis is a heavily used program analysis technique in software engineering. Plenty of static slicing tools are available to support different languages. However, only a few good tools are available for Java program language, such as JavaSlicer, and Slicer4j. I developed a language-agnostic dynamic program slicing tool during my summer'22 internship at the AWS Code Guru team that supports Java, Python, and JavaScript. This tool implements the classic dynamic slicing algorithm proposed by Agrawal and Horgan, 1990. First, execution trace and muGraph (an extended abstract syntax tree) are used to construct a dynamic program dependency graph (DPDG). Next, from the DPDG, a breadth-first traversal is performed w.r.t the slicing criterion to compute the dynamic slice.



## STG-I: A Dynamic Symbolic Constraint Generation Tool Based on LLVM IR


<img src="../assets/img/stg-I.png"
     alt="STG-I"
     width="350"
     height="220"
     style="float: right;" />

This tool operates on LLVM IR and instruments the bitcode to insert additional instructions for recording execution traces. Variables in a program can be declared as symbolic/unknown, and once the program is executed on concrete inputs, symbolic constraints are generated and stored in a file. Generated symbolic constraints can be used to perform dynamic symbolic execution or to compute input domain coverage using quantifcation. 

Details: [GitHub](https://github.com/soneyahossain/STG-I)




