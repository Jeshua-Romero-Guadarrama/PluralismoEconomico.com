

Sergei Kurgalin

Sergei Borzunov

Algebra and

Geometr y

with Python






Algebra and Geometry with Python





Sergei Kurgalin • Sergei Borzunov

Algebra and Geometry

with Python





Sergei Kurgalin

Sergei Borzunov

Digital Technologies Department

Voronezh State University

Voronezh, Russia

Digital Technologies Department

Voronezh State University

Voronezh, Russia

ISBN 978-3-030-61540-6

ISBN 978-3-030-61541-3 (eBook)

<https://doi.org/10.1007/978-3-030-61541-3>

© Springer Nature Switzerland AG 2021

This work is subject to copyright. All rights are reserved by the Publisher, whether the whole or part of

the material is concerned, speciﬁcally the rights of translation, reprinting, reuse of illustrations, recitation,

broadcasting, reproduction on microﬁlms or in any other physical way, and transmission or information

storage and retrieval, electronic adaptation, computer software, or by similar or dissimilar methodology

now known or hereafter developed.

The use of general descriptive names, registered names, trademarks, service marks, etc. in this publication

does not imply, even in the absence of a speciﬁc statement, that such names are exempt from the relevant

protective laws and regulations and therefore free for general use.

The publisher, the authors, and the editors are safe to assume that the advice and information in this book

are believed to be true and accurate at the date of publication. Neither the publisher nor the authors or

the editors give a warranty, expressed or implied, with respect to the material contained herein or for any

errors or omissions that may have been made. The publisher remains neutral with regard to jurisdictional

claims in published maps and institutional afﬁliations.

This Springer imprint is published by the registered company Springer Nature Switzerland AG.

The registered company address is: Gewerbestrasse 11, 6330 Cham, Switzerland





**Preface**

The rapid development of computing places special demands on the training of

young specialists in this ﬁeld. The complexity of the problems that must be

solved to satisfy the needs of science, technology, industry and the economy also

grows, simultaneously with the rapid growth in the power of modern computer

systems. In this connection, we believe that it is essential that computing specialists

have fundamental knowledge about the development of the related mathematical

frameworks and about how to create methods for solving the above problems.

Algebra and geometry are deemed important areas whose ideas and results are

actively used in the development of information systems, as well as in software

developed for business projects. The basic notions of algebra are numerical matrices

and the methods for working with matrix algorithms. They may be used extensively

in scientiﬁc and technical problems and in the game industry. The rapid development

of game technologies, as well as augmented and alternative reality technologies,

means that we must pay special attention to university courses in analytical

geometry and linear algebra, pattern properties in 3D space and fast algorithms for

working with two- and three-dimensional objects.

Another promising area of application for linear algebra algorithms that has seen

rapid development in recent years is Big Data. Analysis of extremely large arrays

requires not only knowledge and use of the known methods, but it also issues the

challenge to develop new approaches and high-performance algorithms.

This textbook is an introduction to linear algebra and analytical geometry for

higher-education students in the natural sciences. It is based on the courses Algebra

and Geometry, Analytical Geometry and Fundamental and Computer Algebra,

which are taught to ﬁrst-year students of the Faculty of Computer Sciences at

the Voronezh State University. The teaching is meant for theoretical training, as

a supplement to the existing textbooks, for practical and laboratory classes, and also

for self-study. Going forward, the terms “Algebra” and “Linear Algebra” will be

considered equivalent, as well as “Geometry” and “Analytical Geometry”.

v





vi

Preface

The authors have attempted to lay the material down in the most comprehensible

form while not sacriﬁcing strictness in deﬁnitions and theorems. The statements

(theorems, properties) are accompanied with proofs, or references to specialist

literature for advanced study of the materials.

The fundamentals of algebra and geometry are presented in the form most

suitable for future specialists in computing. We have considered the basic algorithms

for working with matrices, vectors and systems of linear equations. The theoretical

material contains solutions of most types of problems and is supplemented with

plenty of analysed examples. The end of an example is designated by the symbol

. Each chapter ends with problems for self-study. Many of them are provided not

only with full answers but also with detailed solutions. The asterisk sign (∗) marks

the advanced (enhanced complexity) problems.

Apart from the sections traditionally included in algebra and geometry courses,

one of the chapters is devoted to the mathematical fundamentals of the modern

section of cryptography, namely elliptic curve cryptography. The availability of this

chapter will be a connecting link between the mathematical courses and methods

applied in practice by the application software developers.

The section about quantum computing is devoted to one of the examples of the

application of algebra. It demonstrates that the notions of linear algebra are used for

constructing new algorithms, whose computation capacity exceeds the existing ones

considerably.

Let us brieﬂy summarize the content of this textbook. The ﬁrst four chapters

are devoted to classical divisions of linear algebra; they consider matrices and

determinants, and systems of linear equations; deﬁnitions are given for the notion of

vector space and the fundamental solution of a homogeneous system. The next few

chapters introduce the fundamentals of vector algebra and the coordinate method

on a plane and in a 3D space. The following subjects are considered: vectors in

three-dimensional space, the equation of a line on a plane, the equation of a plane

in space and the equation of a line in space. Second-order curves are analysed.

Material on elliptic curves is usually not included in a “traditional” algebra and

geometry course. However, its presence in this book, in our opinion, contributes to a

deeper understanding of the methods of linear algebra and analytical geometry and

provides an example of the implementation of such methods for solving problems

in theoretical and practical cryptography.

We use the Python programming language for illustration of the considered

algorithms. This allows us to familiarize readers with implementation at the initial

stage of study. Python was selected because it is a universal and widely used general-

purpose programming language, suitable for the successful realization of numerical

algorithms; Python is a continuously evolving language; and many of its realizations

are open source. Python has the necessary tools to automatically check for the

errors that might appear in the program code in the process of its creation. The

availability of a great number of additional libraries (such as NumPy, SciPy, pandas)

substantially expands the programmer’s capabilities. Thus, this language is quite

suitable for teaching linear algebra and analytical geometry algorithms.





Preface

vii

As the time of writing, the version of Python known as “Python 2” is still being

used in many signiﬁcant projects and in the literature. However, ofﬁcial support for

Python 2 is diminishing and is scheduled to end. So, we use the latest major version,

“Python 3”, in this book. Note that there are signiﬁcant differences between Python

2 and Python 3; however, extended support documentation and tools are available

for conversion between the two major versions. Refer to the ofﬁcial Python webpage

(<https://www.python.org/>) for more details.

The book offers a list of training literature on linear algebra and analytical

geometry, which may be used for a more detailed study on the issues touched upon

in this textbook.

The appendices contain reference information, including basic operators in

Python and C, trigonometric formulae and the Greek alphabet. These reduce the

necessity to address reference literature.

Below you can see the chart of the chapter information dependence in the form of

an oriented graph reﬂecting the preferable order of covering the academic material.

For instance, after having studied Chaps. [1](#br16), [2](#br57)[ ](#br57)and [3](#br136), you can move to one of the two

chapters, Chap. [4](#br185)[ ](#br185)or Chap. [6](#br266), the contents of which are relatively independent. After

Chap. [9](#br330), we think Chaps. [11](#br366)[ ](#br366)and [12](#br391)[ ](#br391)can be mastered in any order.





viii

Preface

Chapter 1

Chapter 2

Chapter 3

Chapter 4

Chapter 5

Chapter 6

Chapter 7

Chapter 8

Chapter 9

Chapter 10

Chapter 11

Chapter 12

The chapter dependency chart





Preface

ix

**Acknowledgements**

The authors express sincere gratitude to their colleagues for useful discussions

and critical remarks. Very useful to the improvement of the text were the valuable

remarks of Artem Atanov, Alexey Bukhovets, Tatiana Churakova, Andrei Fediakov,

Evgenii Kiselev, Alexander Loboda, Pavel Lukin, Peter Meleshenko, Leonid Minin,

Mikhail Semenov and Sergei Zapryagaev.

Enormous help at all stages of working on this book was provided by the experts

at Springer. We are especially grateful to editors Aliaksandr Birukou, Ronan Nugent

and Wayne Wheeler in collaboration with whom we have been fruitfully working

on this and our previous books. Checking of the program code located in the book

was performed with the assistance of students of the Faculty of Computer Sciences,

Voronezh State University—Anna Danilova, Artem Konovskoy, Nikolai Paukov,

Margarita Tepliakova, Vladimir Ushakov and Sergei Zaitsev.

The manuscript of this book was used as the basic teaching for the students at

the Voronezh State University, for several semesters. Their interest and enthusiasm

had a positive inﬂuence on the content of the training course. We thank all the

students who took the course in algebra and geometry, and for helping to eradicate

some of the misprints and mistakes found in the ﬁrst versions of the manuscript.

Great help in checking the solutions and answers to the problems and exercises was

rendered by students Pavel Burdyug, Dmitry Demianov, Kirill Ganigin, Elizaveta

Koroteyeva, Zakhar Korsakov, Denis Makushin, Pavel Nekrasov, Natalya Salova,

Anna Tsybulskaia, Dmitry Tynyanyy and Anna Yankevich.

Of course, all other mistakes remaining in the text are exclusively on the authors’

conscience.

Sergei Kurgalin is especially grateful to Olga Kurgalina and Alexander Shirokov

for their constant support during the work on the book.

Voronezh, Russia

Voronezh, Russia

July 2019

Sergei Kurgalin

Sergei Borzunov





**Contents**

[**1**](#br16)

[**Matrices**](#br16)[** ](#br16)[and**](#br16)[** ](#br16)[Matrix**](#br16)[** ](#br16)[Algorithms**](#br16)[** ](#br16).........................................

[1.1](#br16)[ ](#br16)[Matrices](#br16)[ ](#br16)[and](#br16)[ ](#br16)[Operations](#br16)[ ](#br16)[with](#br16)[ ](#br16)[Them](#br16)[ ](#br16)................................

1

1

[1.2](#br27)[ ](#br27)[Concept](#br27)[ ](#br27)[of](#br27)[ ](#br27)[Algorithm,](#br27)[ ](#br27)[Correctness](#br27)[ ](#br27)[of](#br27)[ ](#br27)[Algorithms](#br27)[ ](#br27)................. 12

[1.3](#br28)[ ](#br28)[Estimation](#br28)[ ](#br28)[of](#br28)[ ](#br28)[Algorithm](#br28)[ ](#br28)[Efﬁciency](#br28)[ ](#br28)................................. 13

[1.4](#br30)[ ](#br30)[Primitive](#br30)[ ](#br30)[Matrix](#br30)[ ](#br30)[Operations](#br30)[ ](#br30)[in](#br30)[ ](#br30)[Python](#br30).............................. 15

[1.4.1](#br33)[ ](#br33)[NumPy](#br33)[ ](#br33)[Library](#br33)[ ](#br33)............................................. 18

[1.5](#br33)[ ](#br33)[Matrix](#br33)[ ](#br33)[Algorithms](#br33)[ ](#br33)[in](#br33)[ ](#br33)[the](#br33)[ ](#br33)[Graph](#br33)[ ](#br33)[Theory](#br33)[ ](#br33)............................ 18

[Review](#br38)[ ](#br38)[Questions](#br38)[ ](#br38)............................................................ 23

[Problems](#br39)[ ](#br39)..................................................................... 24

[Answers](#br46)[ ](#br46)[and](#br46)[ ](#br46)[Solutions](#br46)[ ](#br46)...................................................... 31

[**2**](#br57)

[**Matrix**](#br57)[** ](#br57)[Algebra**](#br57)[** ](#br57)............................................................. 43

[2.1](#br57)[ ](#br57)[Determinant](#br57)[ ](#br57)[of](#br57)[ ](#br57)[a](#br57)[ ](#br57)[Matrix:](#br57)[ ](#br57)[Determinants](#br57)[ ](#br57)[of](#br57)[ ](#br57)[the](#br57)[ ](#br57)[Second](#br57)[ ](#br57)[and](#br57)

[Third](#br57)[ ](#br57)[Order](#br57)[ ](#br57)[...........................................................](#br57)[ ](#br57)43

[2.2](#br59)[ ](#br59)[Determinants](#br59)[ ](#br59)[of](#br59)[ ](#br59)[the](#br59)[ ](#br59)[n](#br59)[-th](#br59)[ ](#br59)[order:](#br59)[ ](#br59)[Minors](#br59)[ ](#br59)............................. 45

[2.3](#br62)[ ](#br62)[General](#br62)[ ](#br62)[Properties](#br62)[ ](#br62)[of](#br62)[ ](#br62)[Determinants:](#br62)[ ](#br62)[Elementary](#br62)

[Transformations](#br62)[ ](#br62)[of](#br62)[ ](#br62)[a](#br62)[ ](#br62)[Matrix](#br62)[ ](#br62)[.........................................](#br62)[ ](#br62)48

[2.4](#br62)[ ](#br62)[Inverse](#br62)[ ](#br62)[Matrix](#br62)[ ](#br62)[........................................................](#br62)[ ](#br62)50

[2.5](#br66)[ ](#br66)[Integer](#br66)[ ](#br66)[Powers](#br66)[ ](#br66)[of](#br66)[ ](#br66)[a](#br66)[ ](#br66)[Matrix](#br66)........................................... 52

[2.5.1](#br67)[ ](#br67)[Mathematical](#br67)[ ](#br67)[Induction](#br67)[ ](#br67)[Method](#br67)[ ](#br67)........................... 53

[2.6](#br70)[ ](#br70)[Functions](#br70)[ ](#br70)[of](#br70)[ ](#br70)[Matrices](#br70)[ ](#br70)................................................ 56

[2.6.1](#br71)[ ](#br71)[Exponent](#br71)[ ](#br71)[and](#br71)[ ](#br71)[Logarithm](#br71)[ ](#br71)................................... 57

[2.7](#br73)[ ](#br73)[Matrix](#br73)[ ](#br73)[Rank](#br73)[ ](#br73).......................................................... 59

[Review](#br79)[ ](#br79)[Questions](#br79)[ ](#br79)............................................................ 65

[Problems](#br79)[ ](#br79)..................................................................... 65

[Answers](#br91)[ ](#br91)[and](#br91)[ ](#br91)[Solutions](#br91)[ ](#br91)...................................................... 77

[**3**](#br136)

[**Systems**](#br136)[** ](#br136)[of**](#br136)[** ](#br136)[Linear**](#br136)[** ](#br136)[Equations**](#br136)[** ](#br136).............................................. 123

[3.1](#br137)[ ](#br137)[Cramer’s](#br137)[ ](#br137)[Rule](#br137)[ ](#br137)........................................................ 124

[3.2](#br139)[ ](#br139)[Inverse](#br139)[ ](#br139)[Matrix](#br139)[ ](#br139)[Method](#br139)[ ](#br139)............................................... 126

[3.3](#br141)[ ](#br141)[Gaussian](#br141)[ ](#br141)[Elimination](#br141)[ ](#br141)................................................ 128

[3.4](#br150)[ ](#br150)[Fundamental](#br150)[ ](#br150)[System](#br150)[ ](#br150)[of](#br150)[ ](#br150)[Solutions](#br150)[ ](#br150)[of](#br150)[ ](#br150)[Homogeneous](#br150)[ ](#br150)[Systems](#br150)[ ](#br150)..... 137

xi





xii

Contents

[3.5](#br155)[ ](#br155)[General](#br155)[ ](#br155)[Solution](#br155)[ ](#br155)[of](#br155)[ ](#br155)[the](#br155)[ ](#br155)[Non-homogeneous](#br155)[ ](#br155)[System](#br155)

[of](#br155)[ ](#br155)[Equations](#br155)[ ](#br155)[..........................................................](#br155)[ ](#br155)142

[Review](#br155)[ ](#br155)[Questions](#br155)[ ](#br155)[............................................................](#br155)[ ](#br155)145

[Problems](#br159)[ ](#br159)..................................................................... 146

[Answers](#br164)[ ](#br164)[and](#br164)[ ](#br164)[Solutions](#br164)[ ](#br164)...................................................... 151

[**4**](#br185)

[**Complex**](#br185)[** ](#br185)[Numbers**](#br185)[** ](#br185)[and**](#br185)[** ](#br185)[Matrices**](#br185)[** ](#br185)......................................... 173

[4.1](#br185)[ ](#br185)[Arithmetic](#br185)[ ](#br185)[Operations](#br185)[ ](#br185)[with](#br185)[ ](#br185)[Complex](#br185)[ ](#br185)[Numbers](#br185)[ ](#br185).................... 173

[4.2](#br190)[ ](#br190)[Fundamental](#br190)[ ](#br190)[Theorem](#br190)[ ](#br190)[of](#br190)[ ](#br190)[Algebra](#br190)................................... 178

[4.3](#br190)[ ](#br190)[Cardano](#br190)[ ](#br190)[Formula](#br190)[ ](#br190)..................................................... 178

[4.4](#br192)[ ](#br192)[Complex](#br192)[ ](#br192)[Coefﬁcient](#br192)[ ](#br192)[Matrices](#br192)[ ](#br192)....................................... 180

[4.4.1](#br192)[ ](#br192)[Hermitian](#br192)[ ](#br192)[Matrices](#br192)[ ](#br192)......................................... 180

[4.4.2](#br194)[ ](#br194)[Unitary](#br194)[ ](#br194)[Matrices](#br194)[ ](#br194)............................................ 182

[4.5](#br195)[ ](#br195)[Fundamentals](#br195)[ ](#br195)[of](#br195)[ ](#br195)[Quantum](#br195)[ ](#br195)[Computing](#br195).............................. 183

[4.5.1](#br197)[ ](#br197)[Pauli](#br197)[ ](#br197)[Matrices](#br197)[ ](#br197)[and](#br197)[ ](#br197)[Dirac](#br197)[ ](#br197)[Matrices](#br197)......................... 185

[4.5.2](#br198)[ ](#br198)[Basic](#br198)[ ](#br198)[Operations](#br198)[ ](#br198)[with](#br198)[ ](#br198)[Qubits](#br198)[ ](#br198).............................. 186

[Review](#br203)[ ](#br203)[Questions](#br203)[ ](#br203)............................................................ 191

[Problems](#br204)[ ](#br204)..................................................................... 192

[Answers](#br213)[ ](#br213)[and](#br213)[ ](#br213)[Solutions](#br213)[ ](#br213)...................................................... 201

[**5**](#br228)

[**6**](#br266)

[**Vector**](#br228)[** ](#br228)[Spaces**](#br228)................................................................ 217

[5.1](#br229)[ ](#br229)[Linear](#br229)[ ](#br229)[Dependence](#br229)[ ](#br229)[of](#br229)[ ](#br229)[Vectors](#br229)[ ](#br229)[in](#br229)[ ](#br229)[the](#br229)[ ](#br229)[Space](#br229)[ ](#br229)[R](#br229)[n](#br229)[ ](#br229)..................... 218

[5.2](#br230)[ ](#br230)[Basis](#br230)[ ](#br230)[in](#br230)[ ](#br230)[the](#br230)[ ](#br230)[Space](#br230)[ ](#br230)[R](#br230)[n](#br230)[ ](#br230)................................................ 219

[5.3](#br234)[ ](#br234)[Euclidean](#br234)[ ](#br234)[Vector](#br234)[ ](#br234)[Space](#br234)[ ](#br234).............................................. 223

[5.4](#br236)[ ](#br236)[Eigenvalues](#br236)[ ](#br236)[and](#br236)[ ](#br236)[Eigenvectors](#br236)[ ](#br236)[of](#br236)[ ](#br236)[a](#br236)[ ](#br236)[Matrix](#br236)[ ](#br236).......................... 225

[Review](#br242)[ ](#br242)[Questions](#br242)[ ](#br242)............................................................ 231

[Problems](#br242)[ ](#br242)..................................................................... 231

[Answers](#br247)[ ](#br247)[and](#br247)[ ](#br247)[Solutions](#br247)[ ](#br247)...................................................... 236

[**Vectors**](#br266)[** ](#br266)[in**](#br266)[** ](#br266)[a**](#br266)[** ](#br266)[Three-Dimensional**](#br266)[** ](#br266)[Space**](#br266)[** ](#br266)................................... 255

[6.1](#br267)[ ](#br267)[Cartesian](#br267)[ ](#br267)[Coordinate](#br267)[ ](#br267)[System](#br267)[ ](#br267)........................................ 256

[6.2](#br269)[ ](#br269)[Scalar](#br269)[ ](#br269)[Product](#br269)[ ](#br269)[of](#br269)[ ](#br269)[Vectors](#br269)[ ](#br269)............................................ 258

[6.3](#br271)[ ](#br271)[Vector](#br271)[ ](#br271)[Product](#br271)[ ](#br271)[of](#br271)[ ](#br271)[Vectors](#br271)[ ](#br271)............................................ 260

[6.3.1](#br271)[ ](#br271)[Properties](#br271)[ ](#br271)[of](#br271)[ ](#br271)[the](#br271)[ ](#br271)[Vector](#br271)[ ](#br271)[Product](#br271)[ ](#br271)........................... 260

[6.4](#br274)[ ](#br274)[Scalar](#br274)[ ](#br274)[Triple](#br274)[ ](#br274)[Product](#br274)[ ](#br274)................................................. 263

[6.4.1](#br274)[ ](#br274)[Properties](#br274)[ ](#br274)[of](#br274)[ ](#br274)[Scalar](#br274)[ ](#br274)[Triple](#br274)[ ](#br274)[Product](#br274)[ ](#br274)........................ 263

[6.5](#br276)[ ](#br276)[Vector](#br276)[ ](#br276)[Triple](#br276)[ ](#br276)[Product](#br276)[ ](#br276)................................................ 265

[Review](#br277)[ ](#br277)[Questions](#br277)[ ](#br277)............................................................ 266

[Problems](#br277)[ ](#br277)..................................................................... 266

[Answers](#br279)[ ](#br279)[and](#br279)[ ](#br279)[Solutions](#br279)[ ](#br279)...................................................... 268

[**7**](#br287)

[**Equation**](#br287)[** ](#br287)[of**](#br287)[** ](#br287)[a**](#br287)[** ](#br287)[Straight**](#br287)[** ](#br287)[Line**](#br287)[** ](#br287)[on**](#br287)[** ](#br287)[a**](#br287)[** ](#br287)[Plane**](#br287)[** ](#br287).................................. 277

[7.1](#br287)[ ](#br287)[Slope-Intercept](#br287)[ ](#br287)[Form](#br287)[ ](#br287)[of](#br287)[ ](#br287)[the](#br287)[ ](#br287)[Equation](#br287)[ ](#br287)[of](#br287)[ ](#br287)[a](#br287)[ ](#br287)[Straight](#br287)[ ](#br287)[Line](#br287)........... 277

[7.2](#br288)[ ](#br288)[General](#br288)[ ](#br288)[Equation](#br288)[ ](#br288)[of](#br288)[ ](#br288)[a](#br288)[ ](#br288)[Straight](#br288)[ ](#br288)[Line](#br288)................................. 278

[7.3](#br289)[ ](#br289)[Slope-Intercept](#br289)[ ](#br289)[Form](#br289)[ ](#br289)[of](#br289)[ ](#br289)[the](#br289)[ ](#br289)[Equation](#br289)[ ](#br289)[of](#br289)[ ](#br289)[a](#br289)[ ](#br289)[Straight](#br289)[ ](#br289)[Line](#br289)

[Through](#br289)[ ](#br289)[a](#br289)[ ](#br289)[Given](#br289)[ ](#br289)[Point](#br289)[ ](#br289)[...............................................](#br289)[ ](#br289)279

[7.4](#br289)[ ](#br289)[Equation](#br289)[ ](#br289)[of](#br289)[ ](#br289)[a](#br289)[ ](#br289)[Straight](#br289)[ ](#br289)[Line](#br289)[ ](#br289)[Through](#br289)[ ](#br289)[Two](#br289)[ ](#br289)[Given](#br289)[ ](#br289)[Points](#br289)[ ](#br289)[...........](#br289)[ ](#br289)280





Contents

xiii

[7.5](#br291)[ ](#br291)[Angle](#br291)[ ](#br291)[Between](#br291)[ ](#br291)[Two](#br291)[ ](#br291)[Straight](#br291)[ ](#br291)[Lines](#br291)[ ](#br291)................................. 281

[7.6](#br292)[ ](#br292)[Intercept](#br292)[ ](#br292)[Form](#br292)[ ](#br292)[of](#br292)[ ](#br292)[the](#br292)[ ](#br292)[Equation](#br292)[ ](#br292)[of](#br292)[ ](#br292)[a](#br292)[ ](#br292)[Straight](#br292)[ ](#br292)[Line](#br292)[ ](#br292).................. 282

[7.7](#br293)[ ](#br293)[Normal](#br293)[ ](#br293)[(Symmetric)](#br293)[ ](#br293)[Form](#br293)[ ](#br293)[of](#br293)[ ](#br293)[the](#br293)[ ](#br293)[Equation](#br293)[ ](#br293)[of](#br293)[ ](#br293)[a](#br293)[ ](#br293)[Line](#br293)[ ](#br293).............. 283

[7.8](#br297)[ ](#br297)[Line](#br297)[ ](#br297)[Segments](#br297)[ ](#br297)........................................................ 287

[Review](#br300)[ ](#br300)[Questions](#br300)[ ](#br300)............................................................ 290

[Problems](#br300)[ ](#br300)..................................................................... 290

[Answers](#br303)[ ](#br303)[and](#br303)[ ](#br303)[Solutions](#br303)[ ](#br303)...................................................... 293

[**8**](#br316)

[**Equation**](#br316)[** ](#br316)[of**](#br316)[** ](#br316)[a**](#br316)[** ](#br316)[Plane**](#br316)[** ](#br316)[in**](#br316)[** ](#br316)[Space**](#br316)[** ](#br316).............................................. 307

[8.1](#br316)[ ](#br316)[Equation](#br316)[ ](#br316)[of](#br316)[ ](#br316)[a](#br316)[ ](#br316)[Plane](#br316)[ ](#br316)[That](#br316)[ ](#br316)[Is](#br316)[ ](#br316)[Orthogonal](#br316)[ ](#br316)[to](#br316)[ ](#br316)[the](#br316)[ ](#br316)[Speciﬁed](#br316)

[Vector](#br316)[ ](#br316)[and](#br316)[ ](#br316)[Passes](#br316)[ ](#br316)[Through](#br316)[ ](#br316)[the](#br316)[ ](#br316)[Speciﬁed](#br316)[ ](#br316)[Point](#br316)[.....................](#br316)[ ](#br316)307

[8.2](#br316)[ ](#br316)[General](#br316)[ ](#br316)[Equation](#br316)[ ](#br316)[of](#br316)[ ](#br316)[a](#br316)[ ](#br316)[Plane](#br316)[ ](#br316)[.........................................](#br316)[ ](#br316)308

[8.3](#br318)[ ](#br318)[Intercept](#br318)[ ](#br318)[Form](#br318)[ ](#br318)[of](#br318)[ ](#br318)[the](#br318)[ ](#br318)[Equation](#br318)[ ](#br318)[of](#br318)[ ](#br318)[a](#br318)[ ](#br318)[Plane](#br318)[ ](#br318).......................... 309

[8.4](#br319)[ ](#br319)[Normal](#br319)[ ](#br319)[Equation](#br319)[ ](#br319)[of](#br319)[ ](#br319)[a](#br319)[ ](#br319)[Plane](#br319)[ ](#br319)......................................... 310

[8.5](#br320)[ ](#br320)[Equation](#br320)[ ](#br320)[of](#br320)[ ](#br320)[a](#br320)[ ](#br320)[Plane](#br320)[ ](#br320)[That](#br320)[ ](#br320)[Passes](#br320)[ ](#br320)[Through](#br320)[ ](#br320)[the](#br320)[ ](#br320)[Speciﬁed](#br320)

[Point](#br320)[ ](#br320)[Parallel](#br320)[ ](#br320)[to](#br320)[ ](#br320)[the](#br320)[ ](#br320)[Two](#br320)[ ](#br320)[Speciﬁed](#br320)[ ](#br320)[Vectors](#br320)[ ](#br320)[.........................](#br320)[ ](#br320)311

[8.6](#br320)[ ](#br320)[Equation](#br320)[ ](#br320)[of](#br320)[ ](#br320)[the](#br320)[ ](#br320)[Plane](#br320)[ ](#br320)[That](#br320)[ ](#br320)[Passes](#br320)[ ](#br320)[Through](#br320)[ ](#br320)[the](#br320)[ ](#br320)[Three](#br320)

[Speciﬁed](#br321)[ ](#br321)[Points](#br321)[ ](#br321)[......................................................](#br321)[ ](#br321)312

[8.7](#br321)[ ](#br321)[Angle](#br321)[ ](#br321)[Between](#br321)[ ](#br321)[Two](#br321)[ ](#br321)[Planes](#br321)[..........................................](#br321)[ ](#br321)312

[8.8](#br322)[ ](#br322)[Distance](#br322)[ ](#br322)[from](#br322)[ ](#br322)[a](#br322)[ ](#br322)[Point](#br322)[ ](#br322)[to](#br322)[ ](#br322)[a](#br322)[ ](#br322)[Plane](#br322)..................................... 313

[8.9](#br322)[ ](#br322)[Pencil](#br322)[ ](#br322)[of](#br322)[ ](#br322)[Planes](#br322)....................................................... 313

[Review](#br323)[ ](#br323)[Questions](#br323)[ ](#br323)............................................................ 314

[Problems](#br323)[ ](#br323)..................................................................... 314

[Answers](#br324)[ ](#br324)[and](#br324)[ ](#br324)[Solutions](#br324)[ ](#br324)...................................................... 315

[**9**](#br330)

[**Equation**](#br330)[** ](#br330)[of**](#br330)[** ](#br330)[a**](#br330)[** ](#br330)[Line**](#br330)[** ](#br330)[in**](#br330)[** ](#br330)[a**](#br330)[** ](#br330)[Space**](#br330)[** ](#br330)............................................. 321

[9.1](#br330)[ ](#br330)[Equation](#br330)[ ](#br330)[of](#br330)[ ](#br330)[a](#br330)[ ](#br330)[Line](#br330)[ ](#br330)[That](#br330)[ ](#br330)[Passes](#br330)[ ](#br330)[Through](#br330)[ ](#br330)[the](#br330)[ ](#br330)[Speciﬁed](#br330)[ ](#br330)[Point](#br330)

[Parallel](#br330)[ ](#br330)[to](#br330)[ ](#br330)[the](#br330)[ ](#br330)[Speciﬁed](#br330)[ ](#br330)[Vector](#br330)[ ](#br330)[......................................](#br330)[ ](#br330)321

[9.2](#br330)[ ](#br330)[Equation](#br330)[ ](#br330)[of](#br330)[ ](#br330)[a](#br330)[ ](#br330)[Line](#br330)[ ](#br330)[That](#br330)[ ](#br330)[Passes](#br330)[ ](#br330)[Through](#br330)[ ](#br330)[the](#br330)[ ](#br330)[Two](#br330)[ ](#br330)[Speciﬁed](#br330)

[Points](#br332)[ ](#br332)[.................................................................](#br332)[ ](#br332)323

[9.3](#br332)[ ](#br332)[Angle](#br332)[ ](#br332)[Between](#br332)[ ](#br332)[Two](#br332)[ ](#br332)[Lines](#br332)[ ](#br332)[...........................................](#br332)[ ](#br332)323

[9.4](#br333)[ ](#br333)[Angle](#br333)[ ](#br333)[Between](#br333)[ ](#br333)[a](#br333)[ ](#br333)[Line](#br333)[ ](#br333)[and](#br333)[ ](#br333)[a](#br333)[ ](#br333)[Plane](#br333)[ ](#br333).................................. 324

[9.5](#br335)[ ](#br335)[Condition](#br335)[ ](#br335)[of](#br335)[ ](#br335)[Two](#br335)[ ](#br335)[Lines’](#br335)[ ](#br335)[Belonging](#br335)[ ](#br335)[to](#br335)[ ](#br335)[a](#br335)[ ](#br335)[Plane](#br335)[ ](#br335)..................... 326

[Review](#br337)[ ](#br337)[Questions](#br337)[ ](#br337)............................................................ 328

[Problems](#br337)[ ](#br337)..................................................................... 328

[Answers](#br339)[ ](#br339)[and](#br339)[ ](#br339)[Solutions](#br339)[ ](#br339)...................................................... 330

[**10**](#br344)[** ](#br344)[Bilinear**](#br344)[** ](#br344)[and**](#br344)[** ](#br344)[Quadratic**](#br344)[** ](#br344)[Forms**](#br344)[** ](#br344)............................................ 335

[10.1](#br344)[ ](#br344)[Bilinear](#br344)[ ](#br344)[Forms](#br344)........................................................ 335

[10.2](#br346)[ ](#br346)[Quadratic](#br346)[ ](#br346)[Forms](#br346)...................................................... 337

[10.3](#br348)[ ](#br348)[Bringing](#br348)[ ](#br348)[the](#br348)[ ](#br348)[Quadratic](#br348)[ ](#br348)[Form](#br348)[ ](#br348)[to](#br348)[ ](#br348)[the](#br348)[ ](#br348)[Canonical](#br348)[ ](#br348)[Form](#br348)............... 339

[10.3.1](#br349)[ ](#br349)[Lagrange’s](#br349)[ ](#br349)[Method](#br349)[ ](#br349)[of](#br349)[ ](#br349)[Separating](#br349)[ ](#br349)[Perfect](#br349)[ ](#br349)[Squares](#br349)........ 340

[10.3.2](#br352)[ ](#br352)[Jacobi](#br352)[ ](#br352)[Method](#br352)[ ](#br352).............................................. 343

[Review](#br353)[ ](#br353)[Questions](#br353)[ ](#br353)............................................................ 344

[Problems](#br354)[ ](#br354)..................................................................... 345

[Answers](#br355)[ ](#br355)[and](#br355)[ ](#br355)[Solutions](#br355)[ ](#br355)...................................................... 346





xiv

Contents

[**11**](#br366)[** ](#br366)[Curves**](#br366)[** ](#br366)[of**](#br366)[** ](#br366)[the**](#br366)[** ](#br366)[Second**](#br366)[** ](#br366)[Order**](#br366)[** ](#br366)............................................... 357

[11.1](#br366)[ ](#br366)[Ellipse](#br366)................................................................. 357

[11.2](#br369)[ ](#br369)[Hyperbola](#br369)............................................................. 360

[11.3](#br371)[ ](#br371)[Parabola](#br371)............................................................... 362

[11.4](#br372)[ ](#br372)[Degenerate](#br372)[ ](#br372)[Curves](#br372)[ ](#br372)................................................... 363

[11.4.1](#br372)[ ](#br372)[Imaginary](#br372)[ ](#br372)[Ellipse](#br372)[ ](#br372)........................................... 363

[11.4.2](#br373)[ ](#br373)[Pair](#br373)[ ](#br373)[of](#br373)[ ](#br373)[Intersecting](#br373)[ ](#br373)[Lines](#br373)................................... 364

[11.4.3](#br373)[ ](#br373)[Pair](#br373)[ ](#br373)[of](#br373)[ ](#br373)[Imaginary](#br373)[ ](#br373)[Intersecting](#br373)[ ](#br373)[Lines](#br373)....................... 364

[11.4.4](#br373)[ ](#br373)[Pair](#br373)[ ](#br373)[of](#br373)[ ](#br373)[Parallel](#br373)[ ](#br373)[Lines](#br373)[ ](#br373)....................................... 364

[11.4.5](#br374)[ ](#br374)[Pair](#br374)[ ](#br374)[of](#br374)[ ](#br374)[Imaginary](#br374)[ ](#br374)[Parallel](#br374)[ ](#br374)[Lines](#br374)[ ](#br374)........................... 365

[11.4.6](#br374)[ ](#br374)[Pair](#br374)[ ](#br374)[of](#br374)[ ](#br374)[Coincident](#br374)[ ](#br374)[Lines](#br374).................................... 365

[11.5](#br374)[ ](#br374)[Algorithms](#br374)[ ](#br374)[for](#br374)[ ](#br374)[Computing](#br374)[ ](#br374)[the](#br374)[ ](#br374)[Coordinates](#br374)[ ](#br374)[of](#br374)[ ](#br374)[the](#br374)[ ](#br374)[Tangent](#br374)

[Points](#br374)[ ](#br374)[of](#br374)[ ](#br374)[Second](#br374)[ ](#br374)[Order](#br374)[ ](#br374)[Curve](#br374)[ ](#br374)[and](#br374)[ ](#br374)[the](#br374)[ ](#br374)[Straight](#br374)[ ](#br374)[Line](#br374)[ ](#br374)[...............](#br374)[ ](#br374)365

[Review](#br374)[ ](#br374)[Questions](#br374)[ ](#br374)[............................................................](#br374)[ ](#br374)368

[Problems](#br378)[ ](#br378)..................................................................... 369

[Answers](#br379)[ ](#br379)[and](#br379)[ ](#br379)[Solutions](#br379)[ ](#br379)...................................................... 370

[**12**](#br391)[** ](#br391)[Elliptic**](#br391)[** ](#br391)[Curves**](#br391)[** ](#br391).............................................................. 383

[12.1](#br392)[ ](#br392)[Operation](#br392)[ ](#br392)[of](#br392)[ ](#br392)[Multiplication](#br392)[ ](#br392)[of](#br392)[ ](#br392)[the](#br392)[ ](#br392)[Elliptic](#br392)[ ](#br392)[Curve](#br392)[ ](#br392)[Points](#br392)[ ](#br392)........... 384

[12.1.1](#br394)[ ](#br394)[Addition](#br394)[ ](#br394)[of](#br394)[ ](#br394)[a](#br394)[ ](#br394)[Point](#br394)[ ](#br394)[and](#br394)[ ](#br394)[O](#br394).................................. 386

[12.1.2](#br394)[ ](#br394)[Addition](#br394)[ ](#br394)[of](#br394)[ ](#br394)[Two](#br394)[ ](#br394)[Different](#br394)[ ](#br394)[Points](#br394)[ ](#br394).......................... 386

[12.1.3](#br396)[ ](#br396)[Addition](#br396)[ ](#br396)[of](#br396)[ ](#br396)[Two](#br396)[ ](#br396)[Opposite](#br396)[ ](#br396)[Points](#br396)[ ](#br396).......................... 388

[12.1.4](#br396)[ ](#br396)[Duplication](#br396)[ ](#br396)[of](#br396)[ ](#br396)[a](#br396)[ ](#br396)[Point](#br396)[ ](#br396)...................................... 388

[12.2](#br400)[ ](#br400)[Elliptic](#br400)[ ](#br400)[Curves](#br400)[ ](#br400)[with](#br400)[ ](#br400)[Rational](#br400)[ ](#br400)[Points](#br400)[ ](#br400)................................ 392

[12.3](#br402)[ ](#br402)[Implementation](#br402)[ ](#br402)[of](#br402)[ ](#br402)[the](#br402)[ ](#br402)[Addition](#br402)[ ](#br402)[Algorithm](#br402)[ ](#br402)......................... 394

[Review](#br407)[ ](#br407)[Questions](#br407)[ ](#br407)............................................................ 399

[Problems](#br407)[ ](#br407)..................................................................... 399

[Answers](#br409)[ ](#br409)[and](#br409)[ ](#br409)[Solutions](#br409)[ ](#br409)...................................................... 401

[**A**](#br414)

[**B**](#br417)

[**C**](#br419)

[**Basic**](#br414)[** ](#br414)[Operators**](#br414)[** ](#br414)[in**](#br414)[** ](#br414)[Python**](#br414)[** ](#br414)[and**](#br414)[** ](#br414)[C**](#br414)[** ](#br414)......................................... 407

[**Trigonometric**](#br417)[** ](#br417)[Formulae**](#br417)[** ](#br417)................................................... 411

[**The**](#br419)[** ](#br419)[Greek**](#br419)[** ](#br419)[Alphabet**](#br419)........................................................ 413

[**References**](#br420)......................................................................... 415

[**Index**](#br423)............................................................................... 419





**Notation**

N

The set of natural numbers

The set of integers

The set of rational numbers

The set of real numbers

The set of complex numbers

n-dimensional vector space

The empty set

Z

Q

R

C

Rn

∅

A ⇒ B

A ⇔ B

∀x(P (x))

∃x(P (x))

A **and** B

A **or** B

A ≡ B

{a , a , . . . , a }

Logical consequence, or implication

Logical equivalence

For all x, the statement P (x) is true

There exists such x that the statement P (x) is true

Conjunction of logical expressions A and B

Disjunction of logical expressions A and B

Equivalency

The set consisting of the elements a , a , . . . , a

1

2

n

1

2

n

n

ai

The sum a1 + a2 + · · · + an

i=1

n

ai

The product a1a2 . . . an

i=1

A = (a )

Matrix formed by the elements aij

ij

T

Matrix transposed relative to

A

I

A

Identity matrix

O

Zero matrix

δij

[A, B]

Kronecker delta

Commutator of the matrices A and B

Trace of the matrix A

tr A

O(g(n))

G(V , E)

d(v)

Class of functions growing not faster than the function g(n)

G is a graph with vertex set V and edge set E

Degree of vertex v of a graph

D(V , E)

D is a directed graph with vertex set V and edge set E

xv





xvi

Notation

\+

Out-degree of vertex in a digraph

d (v)

−

v

d (v)

In-degree of vertex in a digraph

v

x

Floor function of x, i. e., the greatest integer less than or equal

to the real number x (see deﬁnition on page [78](#br92))

Additional minor of the matrix element placed at the intersec-

tion of the i-th row and the j-th column

Mij

Aij = (−1)i+j Mij

Cofactor of the element

aij

Inverse of the matrix

A

−1

A

i1,i2,...,ik

j1,j2,...,jk

Minor of the -th order (see page [59](#br73))

M

rk A

k

Rank of the matrix A

Exponential of the matrix

A

Logarithm of the matrix A

Imaginary unit

Complex number conjugate of the complex number

Modulus of the complex number z

Argument of the complex number

Hermitian conjugate matrix

Quantum state

eA or exp

ln A

A

√

i = −1

∗

z

z

|z|

argz

ZH

|ψ

|0
, |1

σ1, σ2, σ3

Basic quantum states of the qubit

Pauli matrices

**x** = [x , . . . , x ]

T

Vector of the -dimensional space Rn

n

1

n

**0**

Zero vector

**x**

Xgen.

Xspec.

Euclidean norm of the vector **x**

General solution of a homogeneous system of linear equations

Speciﬁc solution of a non-homogeneous system of linear

equations

PrL **a**

Projection of the vector **a** onto the line L (see page [256](#br267))

Normalized vectors of the Cartesian coordinate system

Orthogonality of the vectors **a** and **b**

Scalar or inner product of vectors

Vectorial or outer product of vectors

Scalar triple product

Vector triple product

Absolute value of the real number x

Sign of the real number x

Normalizing factor (see pages [285](#br295)[ ](#br295)and [311](#br320))

Deviation of a point from a line or a plane

Bilinear form

Quadratic form

Eccentricity of a curve of the second order

Elliptic curve with real points

**i**, **j**, **k**

**a** ⊥ **b**

(**a** · **b**)

**a** × **b**

(**a**, **b**, **c**)

**a**×(**b**×**c**)

abs(x)

sgn(x)

μ

δ

A(**x**, **y**)

ω(**x**)

ε



Elliptic curve with rational points

Point at inﬁnity of an elliptic curve

The sum of two points A and B on an elliptic curve

O

A ⊕ B





**Chapter 1**

**Matrices and Matrix Algorithms**

**1.1 Matrices and Operations with Them**

**Matrix** of size m × n is a rectangular table of numbers with m rows and n columns.

A matrix is written in the form

⎡

⎤

a11 a12 . . . a1n

⎢

⎥

⎢

⎥

⎢a21 a22 . . . a2 ⎥

n

A = ⎢

(1.1)

⎥ .

⎢

⎥

. . . . . . . . . . . . . .

⎣

⎦

a

m m mn

1 a 2 . . . a

Matrices are usually denoted by capital Latin letters, for example, A, B, U, . . .

Numbers aij , included into the matrix, are its **elements**. An ordered set of

elements a , a , . . . , a of the matrix A, having similar ﬁrst index i, is referred

i1 i2

in

to as the i-th **row** of the matrix, while an ordered set of elements a1j , a2j , . . . , amj

,

having similar second index j, is referred to as the j-th **column**. Thus, the ﬁrst

index of an arbitrary element aij indicates the row number, while the second index

indicates the column number, at the intersection of which this element is situated.

A brief matrix record is widely used:

A = (aij ), i = 1, 2, . . . , m; j = 1, 2, . . . , n.

(1.2)

The column of n numbers is also called n-**vector**, or simply **vector**. So, the 1st

vector represents a single number, or, in other words, **scalar**.

© Springer Nature Switzerland AG 2021

1

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_1>





2

1 Matrices and Matrix Algorithms

Note Matrices were initially introduced for a compact record of linear equations.

Now, they are used in various divisions of mathematics and physics and their

applications for simpler presentation of various mathematical operations on matrix

elements.

Example 1.1 A point on a computer screen in RGB format is presented in the form

of a 3-vector with components

⎡

⎤

pR

p

⎢

⎥

P =

⎢

⎥

,

(1.3)

⎣

G⎦

p

B

where p , p , p are real numbers from interval [0, 1], they characterize the inten-

R

G

B

sity of red, green and blue colour components, respectively. Various combinations

of the component values allow obtaining any colour. In particular, vectors

⎡

⎤

⎡

⎤

1

0

0

0.2

0.2

0.6

⎢

⎥

⎢

⎥

P1 =

⎢

⎥ and

P2

= ⎢

⎥

(1.4)

⎣

⎦

⎣

⎦

determine red and dark-blue colours, respectively.

If the condition m = n is met, then the matrix is called **square matrix of order** n.

If the number of rows is not equal to the number of columns, and thus the inequality

m = n is met, then such a matrix is a **rectangular** one.

Note For presentation of matrices, the following notations are also used:

⎛

⎞




a11 a12 . . . a1n

a11 a12 . . . a1 

n

⎜

⎟


⎜

⎟


⎜a21 a22 . . . a2 ⎟

a21 a22 . . . a2 

n

n

or

.

(1.5)

⎜

⎟


⎜

⎟


. . . . . . . . . . . . . .

. . . . . . . . . . . . . .

⎝

⎠






a

1 a 2 . . . a

a 1 a 2 . . . a

m m mn

m

m

mn

The elements of **real** matrices are real numbers from the set R = (−∞, ∞),

while the elements of **complex** matrices are complex numbers.

Note In a standard mathematical notation, the indices of the elements begin with

one: i, j = 1, 2, . . . In many programming languages, including Python and C,

rows and columns are numbered from zero to m − 1 and n − 1, respectively.

This difference should be paid attention to when realizing matrix algorithms in the

mentioned languages.





1.1 Matrices and Operations with Them

3

For the matrix A we will build a new matrix B, where we transpose the rows and

the columns:

⎡

⎤

a11 a21 . . . am

1

⎢

⎥

⎢

⎥

⎢a12 a22 . . . a 2 ⎥

m

B = ⎢

(1.6)

⎥ .

⎢

⎥

. . . . . . . . . . . . . .

⎣

⎦

a1 a2 . . . a

mn

n

n

Such a matrix B is called **transposed** with respect to A and is denoted as AT . As is

easy to see, reapplication of the transposition operation returns to the initial matrix:

(AT )T =

A

.

⎡

⎤

5 0 −4

2 −1 3

Example 1.2 Transposed with respect to the matrix A = ⎣

⎦ is the matrix

⎡

⎤

5

2

⎢

⎥

A

T = ⎢ 0 −1⎥.

⎣

⎦

−4 3

Let A be a square matrix. Its **main diagonal** is a set of elements

a11, a22, . . . , ann, having the same indices, and **secondary diagonal**, or **cross-**

**diagonal**, is the set of elements an1, a , . . . , a1n of the matrix.

(n−1)2

A square matrix is called **diagonal**, if all of her elements located outside the main

diagonal are equal to zero:

⎡

⎤

d1 0 . . . 0

⎢

⎥

⎢

⎥

0 d2 . . . 0

⎢

⎥

(1.7)

⎢

⎥ .

⎢

⎥

. . . . . . . . . .

⎣

⎦

0 0 . . . dn

If in a diagonal matrix of form ([1.7](#br18)) for all values i = 1, 2, . . . , n the equalities

d = 1 are true, then the matrix is called **identity matrix**, or **unit matrix**, and is

i

denoted through I, while of all the elements d = 0, then it is called **zero matrix**,

i

or **null matrix**, and is denoted by O:

⎡

⎤

⎡

⎤

1 0 . . . 0

0 1 . . . 0

. . . . . . . . .

0 0 . . . 1

0 0 . . . 0

0 0 . . . 0

. . . . . . . . .

0 0 . . . 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

I = ⎢

⎥ , O = ⎢

(1.8)

⎥ .

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦





4

1 Matrices and Matrix Algorithms

For notation of the elements of an identity matrix, **Kronecker[**1](#br19)[ ](#br19)symbol** is used,

deﬁned as follows:

1, if i = j,

0, if i = j.

δij

\=

(1.9)

Thus, in symbolic notations, we have I = (δij ), where i, j = 1, 2 . . ., n.

Note Often, in the notation of Kronecker symbol, the indices are divided by

commas: δi,j

.

The matrix A = (a ) is called **upper triangular**, if a = 0 at i > j, i.e. all

ij

ij

the elements, positioned below the main diagonal, are equal to zero. Similarly the

matrix B = (b ) is called **lower triangular**, if b = 0 at i < j, i.e. all the elements

ij

ij

above the main diagonal are equal to 0.

Upper and lower triangular matrices may schematically be denoted as shown in

Fig. [1.1](#br19).

Square matrix A = (a ) is called **symmetric**, if for all values i, j = 1, 2, . . . , n

ij

elements a = a , in other words, all the elements symmetric with respect to the

ij

ji

main diagonal are equal to each other.

Taking into account the notion of transposed matrix, the symmetry condition may

be written in the form of the equality A = AT .

For the **antisymmetric** matrix, the elements a = −aji, where i, j

\=

ij

1, 2, . . ., n.

Let us turn to the notion of equality of matrices. Two matrices A = (a ) and

ij

B = (b ) of size m × n are **equal** to each other if and only if a = b for all i and

ij

ij

ij

j. Thus, the property of equality can only be met for the matrices of the same size.

0

.

A =

,

B =

0

**Fig. 1.1** Schematic notation for upper A and lower B triangular matrices. Highlighted is the

position of the elements other than zero

1Leopold Kronecker (1823–1891), German mathematician.





1.1 Matrices and Operations with Them

5

Example 1.3 Consider two matrices C and D:

⎡

⎤

⎡

⎤

⎦

1

c2

d2 −d

C =

⎣

⎦

,

D

= ⎣

,

(1.10)

−c2 c4

d d2

where c and d are some real numbers.

Equality of matrices C = D is equivalent to the system of equations reﬂecting

equality of separate elements:

⎧

⎪

2 =

1

,

⎪ d

⎪

⎪

⎪

⎨

2

c = −d,

(1.11)

⎪

2

⎪−c = d,

⎪

⎪

⎪

⎩

2

c

4 =

d .

Then, the matrices C and D are equal if and only if the equalities c = ± 1 and

d = −1 are met.

Example 1.4 **Binary matrix** or (0, 1)-**matrix** is called a matrix, whose elements

take values 0 or 1. Let us calculate how many binary matrices of size m × n exist.

Each element of such a matrix may only take two values. Since the matrix

consisting of m rows and n columns has a total of mn elements, then we obtain

2mn ways to assign values to the elements. Hence, the number of binary matrices of

size m × n is 2mn.

Consider the basic operations on matrices. Operations on matrices are introduced

using the well-known arithmetic operations on their elements. Addition and multi-

plication of real numbers are naturally transferred to the matrices and form the basic

operations of **matrix algebra**.

**Sum** of two matrices A = (a ) and B = (b ) of the same size m × n is the

ij

ij

matrix C = (c ) of the same size, consisting of the elements c = a + b . And,

ij

ij

ij

ij

for the sum of matrices, it is written C = A + B.

Note, that one may only add square or rectangular matrices of the same size.

Example 1.5 Given two matrices A and B:

⎡

⎤

⎡

⎤

⎦

2 0 −1

1 3 4

0 5 3

2 1 4

A =

⎣

⎦

,

B

= ⎣

.

(1.12)





6

1 Matrices and Matrix Algorithms

Find their sum A + B, having performed the operations of addition of the

respective elements:

⎡

⎤

⎡

⎤

2 + 0 0 + 5 −1 + 3

1 + 2 3 + 1 4 + 4

2 5 2

A + B =

⎣

⎦ = ⎣

⎦

.

(1.13)

3 4 8

**Product** αA of the real number α and the matrix A = (a ) is the matrix C =

ij

(c ), consisting of the elements c = α · a .

ij

ij

ij

Example 1.6 Assume that the real numbers α = 2, β = −3 are set, and the

⎡

⎤

⎡

⎤

0 −1 2

−2 3 4

0 −2 4

−4 6 8

matrix A = ⎣

⎦. Then αA = 2A = ⎣

⎦, βA = (−3)A =

⎡

⎣

⎤

0 3 −6

6 −9 −12

⎦.

Based on the introduced operations, we may make up a difference of matrices

according to the deﬁnition: A − B = A + (−1)B. Thus, the matrices difference is

nothing but the sum of the ﬁrst summand and the second summand, multiplied by

the number (−1).

Note that for antisymmetric matrix A the equality AT = −A is true.

Example 1.7 Find the difference of the matrices deﬁned in Example [1.5](#br20):

⎡

⎣

⎤

⎡

⎤

⎡

⎤

⎡

⎤

2 0 −1

0 5 3

2 0 −1

0 5 3

A − B =

⎦ − ⎣

⎦ = ⎣

⎦ + −1 ⎣

(

)

⎦

1 3 4

2 1 4

1 3 4

2 1 4

⎡

⎤

⎡

⎤

2 + (−1)0 0 + (−1)5 −1 + (−1)3

1 + (−1)2 3 + (−1)1 4 + (−1)4

2 −5 −4

−1 2

= ⎣

⎦ = ⎣

⎦ .

0

The introduced operations have the following properties that are true for arbitrary

matrices A, B and C and all λ, μ ∈ R:

\1. A + B = B + A (commutativity of addition);

\2. (A + B) + C = A + (B + C) (associativity of addition);

\3. λ(μA) = (λ · μ)A;

\4. λ(A ± B) = λA ± λB;

\5. (λ ± μ)A = λA ± μA;

\6. A + O = O + A = A.





1.1 Matrices and Operations with Them

7

The primary operation of linear algebra is the product of matrices. It, based on

the two initial matrices, allows constructing a new matrix.

In order to introduce this notion, let us ﬁrst consider one special case. The product

of a row of n elements by a column of n elements is the element, equal to the sum

of the products of the respective elements of the raw and the column:

⎡

⎤

⎥

b1

b2

⎢

⎥

` `⎢

⎥

⎢

⎥

= a b + a b + · · · + a b .

(1.14)

⎢

a1 a2 . . . a

1

1

2

2

n n

n ⎢ . ⎥

.

⎣ . ⎦

b

n

Example 1.8 Calculate the product of the row [1, 2, 4, 8, 16] by the column

[16, 8, 4, 2, 1]T :

⎡

⎤

16

⎢

⎥

⎢

⎥

8

⎢

⎥


⎢

⎥

⎢

⎥ = 1 · 16 + 2 · 8 + 4 · 4 + 2 · 8 + 1 · 16 = 80

(1.15)

1 2 4 8 16

4

.

⎢

⎥

⎢

⎥

⎢ 2 ⎥

⎣

⎦

1

Now let us consider the general case of matrices of an arbitrary size.

**Product of the matrix** A = (a ) of size m × n and the matrix B = (b ) of

ij

ij

size n × p is the matrix C = (c ) of size m × p, whose elements are expressed in

ij

accordance with the rule:

n

k=1

cij

\=

a b .

ik kj

(1.16)

The product of matrices is written as C = A · B or C = AB.

Thus, the element cij of the matrix C = AB is the sum of the products of the

elements of the i-th row of the matrix A by the respective elements of the j-th

column of the matrix B (Fig. [1.2](#br23)).





8

1 Matrices and Matrix Algorithms

⎡

⎤

⎡

⎢

⎤

⎥

⎡

⎤

⎥

b1j

⎢

⎥

⎢

⎥

b2j

⎢

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

= ⎢

⎥

⎢

⎥

i

-th ⎢

⎥

⎢

.

⎥

⎢

⎥ i-th

a

i

a

. . . a

cij

⎣

1

2

⎦

.

⎣

⎦

row

i

in

⎢

⎥

row

⎣

⎦

bnj

j-th

j-th

column

column

n

c =

a b

ik kj

ij

k=1

**Fig. 1.2** Multiplication of matrices (a ) and (b )

ij

ij

⎡

⎤

1 2

Example 1.9 Execute the operation of multiplication of matrices ⎣

⎦ and

−3 4

⎡

⎣

⎤

−3 6

5 −4

⎦:

⎡

⎤ ⎡

⎦ ⎣

⎤

⎡

⎤

⎦

1 2

−3 6

5 −4

1 · (−3) + 2 · 5

1 · 6 + 2 · (−4)

(−3) · (−3) + 4 · 5 (−3) · 6 + 4 · (−4)

⎣

⎦ = ⎣

−3 4

⎡

⎤

7 −2

29 −34

= ⎣

⎦ .

(1.17)

Note The deﬁnition of the product of matrices introduced above looks less natural

than the deﬁnition of the sum. However, exactly this method of introducing the

operation of multiplication allows, in matrix algebra, preserving many properties

typical for the product of real numbers.

The following properties are met:

\1. A(B + C) = AB + AC, (B + C)A = BA + CA (distributivity of multiplication

with respect to addition);

\2. (AB)C = A(BC) (associativity of multiplication);

\3. OA = AO = O (property of zero matrix);

\4. IA = AI = A (property of identity matrix).





1.1 Matrices and Operations with Them

9

In the general case, in the product of matrices, their order is essential, which is

demonstrated by the following example.

⎡

⎤

⎡

⎤

2 −1

1 0

3 0

Example 1.10 Let A = ⎣

⎦ and B = ⎣

⎦ .

1 −1

Then we have

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

⎦

2 −1

1 0

3 0

2 · 3 + (−1) · 1 2 · 0 + (−1) · (−1)

5 1

A B =

⎣

⎦ ⎣

⎦ = ⎣

⎦ = ⎣

,

1 −1

1 · 3 + 0 · 1

1 · 0 + 0 · (−1)

3 0

(1.18)

at the same time, the product of matrices, executed in a different order, is equal to

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

3 0

2 −1

1 0

3 · 2 + 0 · 1

3 · (−1) + 0 · 0

6 −3

1 −1

B A =

⎣

⎦ ⎣

⎦ = ⎣

⎦ = ⎣

⎦

.

1 −1

1 · 2 + (−1) · 1 1 · (−1) + (−1) · 0

(1.19)

So, matrix multiplication is **non-commutative**, i.e. when the multipliers are

permuted, the result may change.

As it directly follows from the deﬁnition of matrix product, they can be multiplied

when and only when the number of rows of the ﬁrst multiplier—matrix A, coincides

with the number of rows of the second multiplier—matrix B. We should also note

that the existence of the product AB does not imply the existence of the product

BA.

**Matrix Commutator and Matrix Trace**

Matrices A and B are called **commuting** (or **permutation**), if AB = BA. The

commuting matrices are necessarily square and have the same order.

**Commutator** of two square matrices of the same order is the value

[A, B] = AB − BA.

(1.20)

(1.21)

By deﬁnition for commuting matrices, the condition [A, B] = O is met.

Example 1.11 Calculate [A, B], if

⎡

⎤

⎡

⎤

−1 2 −2

1 0 −1

−1 1 1

2 0 0

⎢

⎥

⎢

⎥

A =

⎢

2

1 −1

⎥

,

B

= ⎢

⎥

.

⎣

⎦

⎣

⎦

−1 −1 −1





10

1

Matrices and Matrix Algorithms

**Solution**

⎡

⎤ ⎡

⎤

⎡

⎤

−1 2 −2

1 0 −1

−1 1 1

2 0 0

−7 2

−1 1 −1

−2 −1 0

3

⎢

⎥ ⎢

⎥

⎢

⎥

AB =

⎢

2

1 −1

⎥ ⎢

⎥ = ⎢

⎥

,

,

(1.22)

(1.23)

⎣

⎦ ⎣

⎦

⎣

⎡

⎦

−1 −1 −1

⎡

⎤ ⎡

⎤

⎤

1 0 −1

−1 2 −2

0

3 −1

⎢

⎥ ⎢

⎥

⎢

⎥

BA = −1 1 1

⎢

⎥ ⎢

2

1 −1

⎥ = ⎢

2 −2 0

⎥

⎣

⎦ ⎣

⎦

⎣

⎦

2 0 0

−1 −1 −1

−2 4 −4

⎡

⎤

−7 −1 4

⎢

⎥

[A, B] = AB − BA = ⎢−3 3 −1⎥ .

(1.24)

⎣

⎦

0 −5 4

Example 1.12 Prove **Jaco[bi**](#br25)[**2](#br25)[ ](#br25)identity**, true for the commutators of any matrices of

size n × n:

[[P, Q], R] + [[Q, R], P] + [[R, P], Q] ≡ O.

(1.25)

**Proof** Use the deﬁnition of commutator [P, Q] = PQ − QP, then

[[P, Q], R] = [PQ − QP, R] = (PQ − QP )R − R(P Q − QP)

= PQR − QPR − RP Q + RQP .

(1.26)

Then, in a similar manner, we will present the remaining summands in the sum:

[[Q, R], P] = QRP − RQP − PQR + P RQ,

[[R, P], Q] = RP Q − PRQ − QRP + QP R.

(1.27)

(1.28)

The sum of the values ([1.26](#br25)[),](#br25)[ ](#br25)([1.27](#br25)[)](#br25)[ ](#br25)[a](#br25)nd ([1.28](#br25)[)](#br25), as is easy to see after reducing

such summands, is equal to zero. Thus, the Jacobi identity is proved.

2Carl Gustav Jacob Jacobi (1804–1851), German mathematician.





1.1 Matrices and Operations with Them

11

**Trace** tr A of the square matrix A = (aij ), where 1  i, j  n, is the sum of its

diagonal elements:

n

tr A =

a .

ii

(1.29)

i=1

Another designation of the matrix A trace is Sp A, from a German word “spur”.

Example 1.13 The trace of the identity matrix I of size n × n is equal to its order:

tr I = n.

**Estimate of the Number of Multiplication Operations When Multiplying**

**Matrices**

In order to estimate the working time of the computing algorithms it is necessary to

know the number of the multiplication operations executed in the program. Let us

determine this number for the matrix multiplication operation.

Let both product matrices be square and have the same order n. Then AB

is the matrix n × n. For calculation of all the result elements we will need n2

multiplications of row by column. The multiplication of row by column contains

exactly n multiplications of real numbers. Hence, in order to determine the product

AB we will need n3 real multiplications.

Note There exist non-elementary algorithms that allow multiplying matrices in a

smaller [number](#br26)[ ](#br26)of operations. Among the most well known of such algorithms is

**Strassen[**3](#br26)[ ](#br26)algorithm**. Note that the advantages of using Strassen algorithm and

similar non-elementary methods of [matrices](#br421)[ ](#br421)multiplication become apparent only

for sufﬁciently large matrix size values [[20](#br421)[\].](#br421)

Modern scientiﬁc and technical tasks, game industry projects, and technologies

of augmented and alternative reality require fast execution of matrix operations on

the mass data. This is why such actions with matrices as transposition, multiplication

and others are presently executed using the parallel programming methods. Working

with matrices on high-performance parallel systems has its own peculiarities associ-

ated with the methods of data presentation in the [comput](#br420)[er](#br422)[ ](#br422)memory and the methods

of interprocessor communication. In the works [\[](#br420)[5](#br420)[,](#br420)[ ](#br420)[27](#br421)[,](#br421)[ ](#br421)[56](#br422)[\]](#br422)[ ](#br422)basic algorithms of matrix

algebra are presented, adapted for application on high-performance comp[utin](#br421)g

systems. The examples of implementation of such algorithms are provided in [[42](#br421)[\].](#br421)

Note As was noted above, the matrix elements are real and complex numbers. Apart

from this, the elements may also be functions on which algebraic operations can

be performed. In such a case we say about **functional matrices**. Later on, unless

otherwise speciﬁed, only numerical matrices are considered.

3Volker Strassen (born 1936), German mathematician.





12

1 Matrices and Matrix Algorithms

**1.2 Concept of Algorithm, Correctness of Algorithms**

In the Sect. [1.4](#br30)[ ](#br30)will be shown algorithms for working with matrices in Python

language. This is why, below we will preliminarily consider the concept of

algorithm and algorithm correctness and show how to estimate their efﬁciency.

**Algorithm** is an exact prescription deﬁning the computational process leading

from the v[aryi](#br421)[ng](#br422)[ ](#br422)[s](#br422)ource data to the result sought for (the data is the ordered set of

symbols) [[48](#br421)[,](#br421)[ ](#br421)[49](#br422)[\].](#br422)[ ](#br422)In other words, an algorithm describes a certain computational

procedure with the help of which a computational problem is solved. As a rule,

the algorit[hm](#br420)[ ](#br420)[is](#br422)[ ](#br422)[u](#br422)sed for solving some class of problems rather than one certain

problem [[16](#br420)[,](#br420)[ ](#br420)[69](#br422)[\].](#br422)[ ](#br422)The term “algorithm” derives from the name of a medieval

mathematician al-Khwarizmi.[4](#br27)

The concept of algorithm belongs to basic fundamental notions of mathematics.

Many researchers use various deﬁnitions of algorithm that differ from each [other.](#br421)

[Ho](#br422)wever, all deﬁnitions express or imply the following **algorithm properties** [[48](#br421)[,](#br421)

[49](#br422)[\].](#br422)

\1. Discreteness. An algorithm must represent a process of problem solving as a

sequential execution of separate steps. Execution of each algorithm step takes

some time, and each operation is only executed wholly and cannot be executed

partly.

\2. Elementary character of steps. The method of execution of each command

should be known and simple enough.

\3. Determinateness (from Latin de¯termina¯re—determine). Each successive step of

the algorithm operation is uniquely determined. The result should be the same

for the same source data.

\4. Directedness. It should be known what to consider as the algorithm operation

result.

\5. Mass character. There must be a possibility to apply the algorithm to all

collections of source data from the certain pre-ﬁxed set.

**Correctness of Algorithms**

Consider the algorithm A that solves a certain computational problem. The pos-

sibility of applying this algorithm in a computer program requires justiﬁcation of

correct problem solution for all input data, i.e. we should carry out the **proof of the**

**algorithm** A **correctness**. For this, we need to trace all changes of the variables’

values that occur as a result of the algorithm’s operation. From the mathematical

point of view, we are talking about establishing the true values of some predicates

describing the variables.

4al-Khwarizmi (Muhammad ibn Mu¯ sa¯ al-Khwa¯rizm¯ı) (about 780–about 850), a distinguished

.

mathematician, astronomer, geographer and philosopher. The term “algebra” derives from the

name of his work containing the general techniques for solving problems reduced to several

algebraic equations [\[](#br420)[9](#br420)].





1.3 Estimation of Algorithm Efﬁciency

13

Assume that P is a predicate true for the input data of the algorithm A, Q is a

predicate taking a true value after completion of A. The introduced predicates are

called **precondition** and **postcondition**, respectively.

Proposition {P}A{Q} means the following: “if operation of the algorithm A

starts from the true value of the predicate P, then it will end at the true value of

Q”. We obtain that the proof of correctness of the algorithm A is equivalent to

the proof of trueness of {P}A{Q}. The p[re-](#br28)[ ](#br28)and postcondition together with the

algorithm itself are referred to as the **Hoare[**5](#br28)[ ](#br28)triple**. The Hoare triple describes how

the execution [of](#br422)[ ](#br422)the given fragment of the computer program changes the state of

computation [[59](#br422)[\].](#br422)

Example 1.14 Let us prove the correctness of the algorithm of exchanging the

values of two variables.

§

Listing 1.1¤

1 # Exchanging of values of variables a and b

2 temp = a

3 a = b

¦

¥

4 b = temp

**Proof** Let the variables a and b take the following values: a = a , b = b .

0

0

Precondition: P = {a = a , b = b }, postcondition: Q = {a = b , b = a }.

0

0

0

0

Substitute the values of the variables a and b into the body of the algorithm A,

which will result in the following values: t emp = a , a = b , b = a . This is

0

0

0

why the predicate {P}A{Q} takes the true value, and thus the correctness of the

algorithm swap(a, b) is proved.

**1.3 Estimation of Algorithm Efﬁciency**

An important task of the algorithm analysis is the estimation of the number

of operations executed by the algorithm over a certain class of input data. The

exact number of elementary operations does not play any signiﬁcant role here,

since it depends on the software implementation of the algorithm, the computer’s

architecture and other factors. This is why the algorithm’s performance [indicator](#br420)[ ](#br420)is

the growth rate of this value with the growth of the input data volume [\[](#br420)[16](#br420)[,](#br420)[ ](#br420)[51](#br422)[\].](#br422)

In order to analyse the algorithm efﬁciency, it is necessary to estimate the

running time of the computer that solves the set problem, as well as the volume of

memory used. The estimate of the running time of the computing system is usually

obtained by calculating the number of elementary operations performed during

computations (such operations are called **basic operations**). With the supposition

5Charles Antony Richard Hoare (born 1934), English scientist specializing in computer science.





14

1 Matrices and Matrix Algorithms

that one elementary operation is performed in a strictly deﬁned time, the function

f (n), deﬁned as the number of operations [duri](#br422)ng computations on input data of size

n, is called a **time-complexity function** [[51](#br422)[\].](#br422)

In algorithm analysis, the number of **basic operations** is estimated, and it is

assumed that ex[ecution](#br422)[ ](#br422)[of](#br422)[ ](#br422)each of the listed below operations takes constant and not

depending on n time [[52](#br422)[\].](#br422)

\1. Binary arithmetic operations (+, −, ∗, /) and operations of comparison of real

numbers (<, , >, , =, =).

\2. Logic operations (**and**, **or**).

\3. Branching operations.

\4. Calculation of the values of elementary functions for relatively small values of

their arguments.

During implementation of matrix algorithms, in most cases the basic operation

is considered as the operation of multiplication of two real numbers.

Let us consider the functions f, g : N → (0, ∞). Assume that g(n) describes the

time complexity of the known algorithm.

It is said that a function f (n) belongs to the class O(g(n)) (read as “big O of

g”), if the growth rate of f (n) does not exceed the growth rate of g(n). We give a

strict deﬁnition: f (n) = O(g(n)), if, for all values of the argument n, starting from

a threshold value n = n , the inequality f (n)  cg(n) is valid for some positive c:

0

O(g(n)) = {f (n): ∃c > 0, n0 ∈ N such that for all n  n0

f (n)  cg(n) is valid}.

(1.30)

The notation f (n) ∈ O(g(n)) can be read as “the function g **majorizes** the

function f ”.

Since O(g(n)) denotes a set of functions growing no faster than the function

g(n), then, in order to indicate that a function belongs to this set, the notation

f (n) ∈ O(g(n)) is used. Another notation is rather common in the literature:

f (n) = O(g(n)), where the equals sign is understood conventionally, namely in

the sense of belonging to the set. The class O(g(n)) are referred also to as the **“big**

O **notation”**.

3

4

Example 1.15 Prove that the asymptotic estimate 3n ∈ O(n ) is true.

**Proof** According to the deﬁnition ([1.30](#br29)) we should prove that there exists a positive

constant c such that starting from some number n , the inequality 3n3  cn4 is met,

0

or (cn − 3)n3  0.

Assume that c = 3, then, starting from n = 1, the last inequality is true. Then,

0

3n3 ∈ O(n4).

Note The notation O(f (t)) is used not only for t → ∞, but may also be generalized

in case of an arbitrary limit value of the argument t → t . For example, the

0

expression

f (t) = O(g(t)) at t → t0

(1.31)





1.4 Primitive Matrix Operations in Python

15

means that the limit of the ration limit of the functions f (t) and g(t) is taken at the

point t = t0:

f (t)

lim

= const  0.

(1.32)

t→t0 g(t)

**1.4 Primitive Matrix Operations in Python**

In the programs in P[ython](#br422)[ ](#br422)language, the matrices are presented in the form of two-

dimensional arrays [\[](#br422)[62](#br422)[\].](#br422)[ ](#br422)For the arrays in Python, a special term “list” is used. List

is an ordered sequence of numbers or other presentable in the computing system’s

memory objects. Thus, the matrix is speciﬁed in the form of a list, whose elements

are lists of the same length. In particular, the matrix

⎡

⎤

11 13 15 17

⎢

⎥

A = −9 −8 −7 −6

⎢

⎥

(1.33)

⎣

⎦

−1 −2 12 14

in a Python program will be presented as

A=[[11, 13, 15, 17], [-9, -8, -7, -6], [-1, -2, 12,

14]]

As is seen, for formation of a list an enumeration of its elements separated by

commas is used. In order to address the matrix elements, square brackets are used,

for example, A[i, j].

Note that the indices of arrays in Python begin from zero rather than one. For

example, for the matrix ([1.33](#br30)) we have the following equalities:

A[0, 0] = 11

A[2, 1] = -2

Note The agreement about zero starting [values](#br421)[ ](#br421)of indices is also used in such

programming languages as C and Java [[39](#br421)[\].](#br421)[ ](#br421)[Howe](#br420)[ve](#br422)r, in Fortran and Pascal

languages, the indices by default begin from one [[12](#br420)[,](#br420)[ ](#br420)[74](#br422)[\].](#br422)

Let us show a program code used for inputting the matrix elements from the

console and outputting the matrix to the console (see Listing 1.2).

§

Listing 1.2¤

1 def read\_matrix\_from\_console():

2

3

4

5

6

n = int(input()) # Number of rows

m = int(input()) # Number of columns

A = []

for i in range(n):





16

1 Matrices and Matrix Algorithms

7

row = input().split()

for j in range(m):

row[j] = int(row[j])

A.append(row)

return A

8

9

10

11

12

13

14 def print\_matrix\_to\_console(A):

15

16

17

18

for row in A:

for elem in row:

print(elem, end=’ ’)

print()

¦

¥

Example of call of functions read\_matrix\_from\_console() and

print\_matrix\_to\_console():

A = read\_matrix\_from\_console()

print\_matrix\_to\_console(A)

The following functions presented in Listing 1.3 perform standard operations on

matrices: addition, multiplication by a number and transposition.

§

¤

Listing 1.3

1 def matrix\_add(A, B):

2

3

if len(A) == len(B) and \

len(A[0]) == len(B[0]):

C = [[0 for j in range(len(A[0]))] \

for i in range(len(A))]

4

5

6

7

for i in range(len(A)):

8

for j in range(len(A[0])):

C[i][j] = A[i][j] + B[i][j]

9

10

11

12

13

return C

14 def matrix\_mult\_by\_scalar(A, alpha):

15

16

17

18

19

20

21

22

23

C = [[0 for j in range(len(A[0]))] \

for i in range(len(A))]

for i in range(len(A)):

for j in range(len(A[0])):

C[i][j] = alpha \* A[i][j]

return C





1.4 Primitive Matrix Operations in Python

17

24

25 def matrix\_subtract(A, B):

26

27

28

29

30

31

32

33

34

35

36

37

if len(A) == len(B) and \

len(A[0]) == len(B[0]):

C = [[0 for j in range(len(A[0]))] \

for i in range(len(A))]

for i in range(len(A)):

for j in range(len(A[0])):

C[i][j] = A[i][j] - B[i][j]

return C

38 def matrix\_transpose(A):

39

40

41

42

43

44

45

46

C = [[0 for j in range(len(A))] \

for i in range(len(A[0]))]

for i in range(len(A)):

for j in range(len(A[0])):

C[j][i] = A[i][j]

¦

¥

return C

An important function calculating the product of matrices by formula ([1.16](#br22)) is

presented in Listing 1.4.

§

Listing 1.4¤

1 # Multiplication of matrices A and B

2 def matrix\_mult(A, B):

3

4

C = [[0 for j in range(len(B[0]))] \

for i in range(len(A))]

5

6

for i in range(len(A)):

for j in range(len(B[0])):

s = 0

7

8

9

10

11

12

13

14

15

for k in range(len(B)):

s += A[i][k] \* B[k][j]

C[i][j] = s

return C

¦

¥





18

1 Matrices and Matrix Algorithms

**Table 1.1** Matrix functions and NumPy procedures

Name

Comment

dot(A,B)

The product of matrices A and B

Trace of matrix

trace(A)

linalg.inv(A)

linalg.det(A)

Inversion of matrix

Determinant of matrix

linalg.matrix\_power(A, n) Raising matrix A to power n

linalg.eigvals(A)

linalg.eig(A)

Calculation of eigenvalues of matrix

Solution of problems on eigenvalues and eigenvectors,

the function return all solutions (λ, X) of the system

AX = λX

linalg.solve(A, B)

Solution of the system of linear equations AX = B with

vector B on its right side

**1.4.1 NumPy Library**

For hi[gh-performance](#br421)[ ](#br421)calculations, the library NumPy with open source code is

widely used [[46](#br421)[,](#br421)[ ](#br421)[57](#br422)[\].](#br422)[ ](#br422)In this package, for presentation of matrices in the memory,

the data type array is introduced. Apart from this, when including NumPy using the

command

from numpy import

\*

a great number of matrix functions and procedures become available. The most

important ones are listed in Table [1.1](#br33).

In particular, transposition of arbitrary rectangular matrices is performed using

the method “.T”:

A=array([[11, 13, 15, 17], [-9, -8, -7, -6], [-1, -2,

12, 14]])

A.T

To the console (more speciﬁcally, into the standard output stream) will be sent

A=array([[11, -9, -1],

[13, -8, -2],

[15, -7, 12],

[17, -6, 14]])

**1.5 Matrix Algorithms in the Graph Theory**

As an example of the algorithm’s operation with mat[rices](#br33), let us [cons](#br420)i[der](#br422)[ ](#br422)one of the

important algorithms of the graph theory—Warshal[l](#br33)[6](#br33)[ ](#br33)algorithm [[1](#br420)[,](#br420)[ ](#br420)[61](#br422)[\],](#br422)[ ](#br422)which is

used for calculating the reachability matrix of the speciﬁed directed graph D(V , E).

6Stephen Warshall (1935–2006), American researcher in the ﬁeld of computer sciences.





1.5 Matrix Algorithms in the Graph Theory

19

First we will recall the basic notions of the graph theory. Everywhere below, the

multiplication operation signs “·” and “×” will be considered as equivalent. In some

cases, when it is clear that we are dealing with multiplication, they may be omitted.

**Graph** is a pair G = (V, E), where V is [the](#br421)[ ](#br421)[set](#br421)[ ](#br421)[of](#br422)[ ](#br422)[v](#br422)[ertices,](#br422)[ ](#br422)while E is the set

of edges, connecting some pairs of vertices [[22](#br421)[,](#br421)[ ](#br421)[31](#br421)[,](#br421)[ ](#br421)[55](#br422)[,](#br422)[ ](#br422)[73](#br422)[\].](#br422)[ ](#br422)In **directed graphs**,

the edges are the ordered pair of vertices, i.e. it is of importance which vertex is the

beginning of the edge and which one is the end. Directed graphs are also referred to

as **digraphs**.

A drawing where the graph vertex is shown as points and the edges are shown as

segments or arcs is called a **graph diagram**.

Two vertices u and v of the graph are **adjacent**, if they are connected by the

edge r = uv. In this case it is said that the vertices u and v are the **endpoints** of the

edge r. If the vertex v is the endpoint of the edge r, then v and r are considered to

be **incident** (from Latin ince¯dere—to distribute).

The number of elements (**cardinality**) of any set, for example V , is denoted as

|V |.

**Adjacency matrix** M is a binary matrix of a relation over the set of vertices of

the graph G(V , E), which is speciﬁed by its edges. The adjacency matrix as the size

|V | × |V |, and its elements are determined in accordance with the rule

1, if edge ij ∈ E,

M(i, j) =

(1.34)

0, if edge ij ∈/ E.

A **path** of length k in the graph G is a sequence of vertices v , v , . . . , v such

0

1

k

that ∀i = 1, . . . , k the vertices v

and vi are adjacent. There are also considered

**trivial** paths of the form v , v . For undirected graphs, paths are also called **routes**.

i−1

i

i

The **length** of the path is the number of edges in it, taking into account the

iterations.

Example 1.16 Consider a digraph D(V , E), the set of vertices V and the set of

edges E of which are speciﬁed as follows:

V = {a, b, c, d, e}, E = {ab, ae, bc, bd, dc, de, ec}.

The graph D(V , E) is presented in Fig. [1.3](#br35).

The adjacency matrix M of the digraph D has the form:

a b c d e

⎡

⎤

a 0 1 0 0 1

⎢

⎥

⎢

⎥

b⎢0 0 1 1 0⎥

(1.35)

⎢

⎥

⎢

⎥

c⎢0 0 0 0 0⎥.

M =

⎢

⎥

⎢0 0 1 0 1⎥

d

⎣

⎦

e 0 0 1 0 0





20

1 Matrices and Matrix Algorithms

**Fig. 1.3** The digraph

D(V, E) to the Example [1.3](#br20)

c

b

d

a

e

**Reachability matrix** M∗ of the digraph D(V , E) is a logic closing matrix by

transitivity relation E. The reachability matrix stores the information about the

existence of paths between the digraph vertices: at the intersection of the i-th row

and the j-the column stands 1 when and only when there exists a path from the

vert[ex](#br421)[ ](#br421)v to v . M∗ may be calculated by a formula using the logical operation

i

j

**or** [[29](#br421)[\]](#br421)

∗

2

n

M = M **or** M **or** . . . **or** M ,

(1.36)

where n is the number of vertices of the directed graph, i.e. n = |V |. Note, that

determining the elements of the matrix M∗ by formula ([1.36](#br35)) is associated with

a considerable volume of calculations, this is why for the digraphs with a great

[number](#br35)[ ](#br35)of vertices, t[he](#br422)[ ](#br422)**Warshall algorithm** is used, also known as the **algorithm**

**of Roy[**7](#br35)**–**Warshall** [[61](#br422)[\].](#br422)

The Warshall algorithm is based on formation of a sequence of auxiliary binary

matrices W(0), W(1), ..., W , where n = |V |. The ﬁrst matrix is set equal to the

(n)

adjacency matrix M of the digraph. The elements W(k), where 1  i, j, k  n, are

ij

calculated by the rule: W(k) = 1, if there exists a path connecting the vertices v

i

ij

and v such that all the inner vertices belong to the set V = {v , v , . . . , v }, and

j

k

1

2

k

W

(k) = 0 otherwise. Note that the inner vertex of the path

P

\=

v , . . . , v , . . . , v

i l j

ij

is any vertex v , 1  l  n, belonging to P, except the ﬁrst v and the last v . The

l

i

j

resulting matrix W(n) appears to be equal to W(n) = M∗, since M = 1 when and

∗

ij

only when there exists the path v , . . . , v , all inner vertices of which are contained

i

j

in V = {v , v , . . . , v }.

1

2

n

The principal moment is that the matrix W(k) can be obtained from W(k−1) as

follows. The path v , . . . , v , containing the inner vertices only from the set V ,

i

j

k

exists when and only when one of the conditions is fulﬁlled:

\1. there exists a path vi, . . . , vj with inner vertices only from Vk−1

{v , v , . . . , vk−1};

\=

1

2

7Bernard Roy (born 1934), French mathematician.





1.5 Matrix Algorithms in the Graph Theory

21

\2. there are paths v , . . . , v and v , . . . , v , also containing inner vertices only

1

k

k

j

from Vk−1

.

We obtain two cases: either Wi(jk−1) = 1, if v is included into the set of vertices

k

−1)

(k−1)

allowed at this stage, or W(k

= 1 and W

= 1. Therefore, using the logical

ik

kj

operations **or** (disjunction) and **and** (conjunction) we may write


(k−1) **or**

(k−1) **and** (k−1)

W

(k) =

W

W

W

kj

.

(1.37)

ij

ij

ik

Let us show a respective algorithm for constructing M∗ by the speciﬁed

adjacency matrix M of size n × n, where n > 1. The intermediate matrices W(k),

where 0  k  n − 1, should not necessarily be stored in memory until the end

of the algorithm’s operation, this is why, in the suggested realization, the elements

(k−1) are substituted by the elements of the subsequent matrix (k).

W

W

§

Listing 1.5¤

1 def Warshall\_algorithm(M):

2

3

n = len(M)

4

W = [[0 for j in range(n)] \

for i in range(n)]

5

6

7

for i in range(n):

for j in range(n):

W[i][j] = M[i][j]

8

9

10

11

12

13

14

15

16

17

for k in range(n):

for i in range(n):

for j in range(n):

W[i][j] = W[i][j] or \

(W[i][k] and W[k][j])

¦

¥

return W

Correctness of algorithm WarshallAlgo can be proved by the method of [math](#br422)-

ematical induction (see the description of this method below on page [53](#br67)) [[61](#br422)[\].](#br422)

Sol[utio](#br422)n of the problem for ﬁnding M∗ is also investigated in Problem [**1.39**](#br44)[** ](#br44)and

in [[61](#br422)[\].](#br422)

Example 1.17 Let digraph D be speciﬁed (Fig. [1.4](#br37)). Construct the reachability

matrix M∗, using Warshall algorithm.





22

1

Matrices and Matrix Algorithms

**Fig. 1.4** Directed graph D

a

b

c

d

**Solution** The matrix W(0) coincides with the adjacency matrix of the digraph and

has the form

a b c d

⎡

⎤

a 0 1 0 0

⎢

⎥

⎢

⎥

b⎢1 0 1 0⎥

W

(0) =

⎢

⎥.

⎢

⎥

c 0 0 0 0

⎣

⎦

d 1 0 1 0

Calculate W(1). If W(0) = 1, then the respective element W is also equal to

(1)

ij

ij

\1)

ij

(0)

1: W( = 1. If Wij = 0, then attention should be paid to the elements of the ﬁrst

row and the ﬁrst column, standing at the intersection with the j-th column and the

i-the row: if W1j

(0) =

W

(0) = 1, then (1) = 1. The condition (0) =

W

W

W

i1

(0) = 1

i1

ij

1j

is fulﬁlled for the two pairs (i, j), namely for i = j = 2 and i = 4, j = 2.

\1)

22

(1)

1

Then, W( = W = 1, and all the rest elements W( ) coincide with the respective

42

elements of the matrix W(0). For illustration, in the notation of the matrix we will

highlight in bold and underline the elements W(1) that have changed values at this

step:

a b c d

⎡

⎤

a 0 1 0 0

⎢

⎥

⎢

⎥

b⎢1 **1** 1 0⎥

W

(1) =

⎢

⎥.

⎢

⎥

c 0 0 0 0

⎣

⎦

d 1 **1** 1 0

Then we will calculate W(2). Consider the second row and the second column

of the matrix W(1). The elements W(1) that are positioned in the same row with the





Review Questions

23

\1)

elements of W( = 1 from the second column and in the same column with the

i2

\1)

1

elements of W( = 1 from the second row, will change their values in W( ) for 1.

2j

\1)

11

(1)

13

2

Such will be the elements W( and W . The rest of the elements W( ) coincide

with the respective elements of the matrix W(1).

a b c d

⎡

⎤

a **1** 1 **1** 0

⎢

⎥

⎢

⎥

b⎢1 1 1 0⎥

W

(2) =

⎢

⎥.

⎢

⎥

c 0 0 0 0

⎣

⎦

d 1 1 1 0

At the next step, the vertex c is added to the set of vertices. This does not result

in appearance of new elements with value 1.

a b c d

⎡

⎤

a 1 1 1 0

⎢

⎥

⎢

⎥

b⎢1 1 1 0⎥

W

(3) =

⎢

⎥.

⎢

⎥

c 0 0 0 0

⎣

⎦

d 1 1 1 0

At the ﬁnal step, we obtain W(4) = W(3), and the reachability matrix of digraph

D will have the form

a b c d

⎡

⎤

a 1 1 1 0

⎢

⎥

⎢

⎥

b⎢1 1 1 0⎥

M∗ =

⎢

⎥.

⎢

⎥

c 0 0 0 0

⎣

⎦

d 1 1 1 0

**Review Questions**

\1. Deﬁne diagonal matrix, upper triangular matrix, lower triangular matrix,

symmetric matrix and binary matrix.

\2. How is the matrix transposition operation performed?





24

1 Matrices and Matrix Algorithms

\3. How is the Kronecker delta determined?

\4. What matrices are called symmetric? antisymmetric?

\5. Formulate the deﬁnition of product of two matrices of size m × n and n × p.

\6. What is the commutator of the matrices A and B?

\7. Deﬁne trace of a square matrix.

\8. What is algorithm?

\9. Enumerate the properties of an algorithm.

\10. How is the algorithm efﬁciency estimated?

\11. Explain the meaning of the notation O(f (n)).

\12. Describe the presentation of matrices in Python.

\13. Enumerate the basic matrix functions and the procedures of NumPy library.

\14. How are graphs presented in the computer memory?

\15. For solution of what problem is the Warshall algorithm used?

**Problems**

⎡

⎤

⎡

⎤

2 1 −1

−2 1 0

**1.1**. Calculate 3A + 2B, where A = ⎣

⎦ , B = ⎣

⎦.

0 1 4

−3 2 2

⎡

⎤

⎡

⎤

1 1

1 −1 0

2 3 4

⎢

⎥

**1.2**. Calculate AB, where A = ⎣

(A B)

⎦ , B = ⎢

⎥. Find BT AT and

2 −1

3 0

⎣

⎦

T .

**1.3**. Let the matrix A = (a ) be of size n × n and the matrix B = (b ) be of

ij

1

2

ij

size n × n . Prove that the following equality is fulﬁlled:

2

1

(AB)T = B A ,

T

T

(1.38)

i.e. the transposed product of two matrices is equal to product of the

transposed matrices in reversed order.

**1.4**. Write the matrices of size 3 × 3, whose elements are determined by the

formulas:

(1) aij = (−1)i+j−1;

i + j + |i − j|

;

(2) bij

\=

2

(3) cij = (i − 2)2 + (j − 2)2;

(4) dij = sin(|i − j|).

Calculate the sum of all elements S of each matrix.





Problems

25

**1.5**. Let A = (a ) be a square matrix of order n  3. Using the summation

ij

symbol , write the following values:

(1) the sum of the elements of the third row;

(2) the sum of the elements of the second column;

(3) the sum of squares of the diagonal elements;

(4) the module of the sum of the elements positioned on the secondary

diagonal.

**1.6**. How to write the sum of the elements of the square matrix positioned above

the main diagonal using the summation sign? How to do this for the elements

positioned below the main diagonal?

**1.7**. A student carrying out an experiment in a chemical laboratory has acciden-

tally spilled a reagent on an algebra notes page, where antisymmetric matrix

was written. As a result, it was impossible to read some of its elements. If we

denote such elements by symbol “?”, the notation will look as

⎡

⎤

0 1 −1 ?

? 0 2 2

? ? ? ?

7 ? 0 ?

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ .

⎢

⎥

⎣

⎦

Restore the unknown elements and write the original matrix.

**1.8**. Determine the number of binary matrices of n rows and n columns that are

(1) symmetric and

(2) antisymmetric

relative to the main diagonal.

**1.9**. Calculate

⎡

⎤

0 0 1

1 1 2

2 2 3

3 3 4

⎡

⎢

⎤

⎥

⎡ ⎤

⎡

⎤

⎢

⎥

−1 −1

3

⎢

⎥

4

1 −2

3 −4

⎢

⎥

a)

⎢ 2 2 ⎥ ⎣ ⎦ ; b) ⎣

⎦ .

⎢

⎥

⎣

⎦

⎢

⎥

1

⎣

⎦

1

1

**1.10**. Consider the binary matrices

⎡

⎤

⎡

⎤

0 1 0

0 0 1

0 1 0

1 0 0

⎢

⎥

⎢

⎥

Q1 = 1 0 0

⎢

⎥

,

Q2

= ⎢

⎥

.

⎣

⎦

⎣

⎦

0 0 1

2

2

Calculate Q Q , Q Q , Q and Q .

1

2

2

1

1

2





26

1 Matrices and Matrix Algorithms

**1.11**. For what matrices D of the second order the square of D2 is equal to the zero

matrix?

**1.12**. Let the matrices L = [−2, −1, 0, 1, 2], M = [0, 2, 4, 6, 8] be speciﬁed.

Calculate the products of LMT and MT L.

**1.13**. The elements of the matrix G = (g ) are determined in accordance with the

ij

rule

1, if i  j,

0, if i < j.

gij

\=

What are the elements of the matrix G2 equal to?

**1.14**. At the examination in linear algebra, a student says that multiplication of two

non-zero matrices will necessarily result in a non-zero matrix. Is the student

right?

∗**1.15.** Let us denote by x the number of processors produced by some plant starting

i

from the beginning of the year. In particular, the plant’s operation during the

ﬁrst month is described by the vector X = [x , x , . . . , x ]T . Determine

1

2

31

the matrix D, which should inﬂuence the X, in order to obtain the vector

Y = [x2 − x1, x3 − x2, . . . , x − x −1]

T :

Y

\=

D X Y

. The vector reﬂects

·

n

n

the daily production capacity gain of the plant.

**1.16**. Calculate the product of the functional matrices A(ψ)B(θ)A(ϕ), if

⎡

⎤

⎡

⎤

cos ϕ sin ϕ 0

1

0

0

⎢

⎥

⎢

⎥

A(ϕ) = − sin ϕ cos ϕ 0

⎢

⎥

,

B(θ)

= ⎢

0 cosθ sin θ

0 − sin θ cos θ

⎥

.

⎣

⎦

⎣

⎦

0

0

1

**1.17**. Calculate the commutator [A, B], if

⎡

⎤

⎡

⎤

7 5 3

6 2 3

5 2 1

1 1 6

⎢

⎥

⎢

⎥

A = 1 3 2

⎢

⎥, = ⎢

B

⎥

.

⎣

⎦

⎣

⎦

2 2 7

**1.18**. Calculate the commutator [A, B], if A is an arbitrary matrix, B = I is

identity matrix of the same order as A.

**1.19**. Consider the matrices

⎡

⎤

⎡

⎤

⎡

⎤

0 −1 0

0 0 0

0 0 −1

0 1 0

0 0 1

0 0 0

⎢

⎥

⎢

⎥

⎢

⎥

P1 = 1 0 0

⎢

⎥

,

P2

= ⎢

⎥

,

P3

= ⎢

⎥

.

(1.39)

⎣

⎦

⎣

⎦

⎣

⎦

0 0 0

−1 0 0

Calculate the commutators [P , P ], [P , P ] and [P , P ].

1

2

2

3

3

1

**1.20**. Is it true that for any square matrices A, B and C of the same size the equality

[A + B, C] = [A, C] + [B, C] is fulﬁlled?





Problems

27

**1.21**. Prove that for any matrices A, B and C of the same size, the identity is true

[AB, C] ≡ A[B, C] + [A, C]B.

(1.40)

**1.22**. Is it true that for any square matrices A, B and C of the same size the equality

[A, [B, C]] = [[A, B], C] is fulﬁlled?

**1.23**. Given the square matrices A and B of the same order. In what case the

equality (A + B)2 = A2 + 2AB + B2 is true?

**1.24**. Is it true that if [A, B] = O and [A, C] = O, then the matrices B and C are

commuting?

**1.25**. Suppose that the sizes of the matrices A, B and C are equal to n × n ,

1

2

n2 × n3 and n3 × n4, respectively. In order to calculate the product of ABC,

the multiplication operations can be executed in two ways: (A · B) · C or

A · (B · C). With what relation between the variables n1, n2, n3 and n4 the

calculation using the ﬁrst method—as (A·B)·C—will require less operations

of multiplication of real numbers in comparison with the second method?

**1.26**. Prove the correctness of the algorithm of change of values of two variables

without using the auxiliary variable.

§

Listing 1.6¤

1 # Exchanging of values of variables a and b

2 # without using the auxiliary variable

3 a = a + b

4 b = a - b

5 a = a - b

¦

¥

**1.27**. Prove the correctness of the algorithm of addition of square matrices.

§

Listing 1.7¤

1 # Addition of matrices A and B

2 def matrix\_add(A, B):

3

4

if len(A) == len(B) and \

len(A[0]) == len(B[0]):

5

C = [[0 for j in range(len(A[0]))] \

for i in range(len(A))]

6

7

8

for i in range(len(A)):

9

for j in range(len(A[0])):

C[i][j] = A[i][j] + B[i][j]

10

11

12

¦

¥

return C

**1.28**. Prove the correctness of the square matrix multiplication algorithm.





28

1

Matrices and Matrix Algorithms

§

Listing 1.8¤

1 # Multiplication of matrices A and B

2 def matrix\_mult(A, B):

3

4

C = [[0 for j in range(len(B[0]))] \

for i in range(len(A))]

5

6

for i in range(len(A)):

for j in range(len(B[0])):

s = 0

7

8

9

10

11

12

13

14

15

for k in range(len(B)):

s += A[i][k] \* B[k][j]

C[i][j] = s

return C

¦

¥

**1.29**. Prove the correctness of the optimized matrix multiplication algorithm.

§

Listing 1.9¤

1 # Optimized multiplication

2 # of matrices a and b

3 def matrix\_mult2(A, B):

4

5

n = len(A)

6

C = [[0 for i in range(n)] \

for j in range(n)]

7

8

9

D = [0 for i in range(n)]

10

11

12

13

14

15

16

17

18

19

20

21

22

23

for i in range(n):

for j in range(n):

s = 0

for k in range(n):

D[k] = B[k][j]

for k in range(n):

s += A[i][k] \* D[k]

C[i][j] = s

return C

¦

¥





Problems

29

Note The considered option of matrix multiplication is optimized in such a

manner as to preliminarily select the elements of the column b(k, j) into the

intermediate array d, which may fully be placed in a fast cache memory.

**1.30**. Determine the number of operations of addition of two numbers executed by

the algorithm matrix\_add for the matrices of size N × N.

**1.31**. Determine the number of operations of addition and multiplication, executed

by the algorithm matrix\_mult for the matrices of size N × N.

**1.32**. Suggest a method to decrease the number of addition operations executed by

the algorithm matrix\_mult.

**1.33**. Let A , A and A be numerical matrices of size 50×25, 25×30 and 30×10,

1

2

3

respectively. Determine the minimal number of multiplication operations

required to calculate the product of A A A by the standard algorithm

1

2

3

matrix\_mult, whose realization for square matrices is presented in

Problem [**1.28**](#br42).

**1.34**. Let A , A , A and A be numerical matrices of size 25 × 10, 10 × 50,

1

2

3

4

50 × 5 and 5 × 30, respectively. Find the minimal number of multiplication

operations, required for calculation of the product of A A A A by the

1

2

3

4

standard algorithm matrix\_mult.

**1.35**. Let A , A , A and A be numerical matrices of size 100 × 20, 20 × 15,

1

2

3

4

15×50 and 50×100, respectively. Find the minimal number of multiplication

operations required for calculation of the product of A A A A by the

1

2

3

4

standard algorithm matrix\_mult.

∗**1.36.** Prove that the number of methods for calculation of the product of the

matrices A A . . . A , m  1, or, in other words, the number of ways

1

2

m+1

to place brackets in this product, where A , A , ..., A

are numerical

, respectively, is equal to

1

× n

2

m+1

matrices of [si](#br44)ze n × n , n × n , ..., n

1

2

2

3

m+1

m+2

the **Catalan[**8](#br44)[ ](#br44)number** C , determined by formula

m

1

Cm

\=

C(2m, m) for all m  1,

(1.41)

m + 1

where C(2m, m) is a binomial coefﬁcient.

**1.37**. Estimate the number of operations executed by Warshall algorithm for

obtaining the reachability matrix of a digraph.

**1.38**. Using the Warshall algorithm, calculate the reachability matrix of the digraph

D, presented in Fig. [1.5](#br45).

**1.39**. One of the ways to modify the Warshall algorithm consists in presentation

of the rows of binary matrices as bit strings. In this case, for calculation of

the elements of the matrices W(k) for 1  i  N, the bitwise operation **or**

is used. Find the number of operation in the bit strings executed by the given

realization of the Warshall algorithm.

8Eugène Charles Catalan (1814–1894), Belgian mathematician.





30

1

Matrices and Matrix Algorithms

**Fig. 1.5** To Problem [**1.38**](#br44)

3

2

4

1

5

**1.40**. Write the analytical expression for the function f (n), represented by the

algorithm:

§

Listing 1.10¤

1 def f(n: int):

2

3

4

5

6

7

8

9

temp = 0

for i in range(1, n + 1):

for j in range(1, n + 1):

for k in range(j, n + 1):

temp += 1

¦

¥

return temp

∗**1.41.** Write the analytical expression for the function g(n), represented by the

algorithm:

§

Listing 1.11¤

1 def g(n: int):

2

3

4

5

6

7

8

9

temp = 0

for i in range(1, n + 1):

for j in range(n, i - 1, -1):

for k in range(1, j + 1):

temp += 1

¦

¥

return temp





Answers and Solutions

31

∗**1.42.** Write the analytical expression for the function h(n), represented by the

algorithm:

§

Listing 1.12¤

1 def h(n: int):

2

3

temp = 0

4

for i in range(1, n + 1):

for j in range(1, i + 1):

for k in range(1, j + 1):

5

6

7

for l in range(1, k + 1):

temp += 1

8

9

¦

¥

10

return temp

**1.43**. Calculate the trace of the matrix A = (a ), where 1  i, j  n, whose

ij

elements are speciﬁed by the formulas:

(1) aij = i + j;

(2) aij = i − j;

2

2

(3) aij = ln(i + j );

(4) aij = max(i, n − j);


1 1

,

i j

(5) aij = min

;

(6) aij = sin(π(i + 2j ));

n

(7) aij

\=

− (i + j);

2

1

(8) aij = i +

.

j

**1.44**. Prove that the trace of the product of the square matrices does not depend on

the order of multipliers: tr (AB) = tr (BA).

**Answers and Solutions**

[**1.1**](#br39)[** ](#br39)Solution.

⎡

⎤

⎡

⎤

6 3 −3

0 3 12

−4 2 0

−6 4 4

We calculate the summands in the sum: 3A = ⎣

We perform the matrix summation operation: 3A + 2B = ⎣

⎦, 2B = ⎣

⎦.

⎡

⎤

2 5 −3

−6 7 16

⎦.





32

1 Matrices and Matrix Algorithms

[**1.2**](#br39)[** ](#br39)Solution.

We will calculate the product AB relying on the formula ([1.16](#br22)) on page [7](#br22):

⎡

⎤

⎡

⎣

⎤

1 1

2 −1

3 0

1 −1 0

⎢

⎥

A · B =

⎦ ⎢

⎥

⎣

⎦

2 3 4

⎡

⎤

⎡

⎤

1 · 1 + (−1) · 2 + 0 · 3 1 · 1 + (−1) · (−1) + 0 · 0

2 · 1 + 3 · 2 + 4 · 3

−1 2

20 −1

= ⎣

⎦ = ⎣

⎦ .

2 · 1 + 3 · (−1) + 4 · 0

We execute the matrix transposition operation:

⎡

⎤

⎡

⎤

1 2

⎢

⎥

1 2 3

T = ⎢−1 3⎥ T = ⎣

, B

⎦ ;

A

⎣

⎦

1 −1 0

0 4

⎡

⎤

⎦

1 · 1 + 2 · (−1) + 3 · 0

1 · 1 + (−1) · (−1) + 0 · 0 1 · 2 + (−1) · 3 + 0 · 4

1 · 2 + 2 · 3 + 3 · 4

BT ·

A

T = ⎣

⎡

⎤

−1 20

2 −1

= ⎣

⎦ .

⎡

⎤

−1 20

2 −1

(A · B)

T = ⎣

⎦

.

Note that the equality (AB)T = BT AT is fulﬁlled for any matrices A and B, for

which the product AB is determined.

[**1.3**](#br39)[** ](#br39)Proof.

Based on the deﬁnition of the matrix transposition and on the formula ([1.16](#br22)), the

left part of the equality ([1.38](#br39)) consists of elements:

n1

k=1


(AB)T

\=

(AB)ji

\=

a b ,

jk ki

ij

where 1  i  n , 1  j  n .

3

1

Further, we represent elements of the right side of Eq.[(](#br39)[1.38](#br39)) in the form

n2

k=1

n2

k=1

n2

k=1

T

(B A )

T

\=

T

(B ) (A )

T

\=

\=

b a

ki jk

a b ,

jk ki

ij

ik

kj

where 1  i  n , 1  j  n .

3

1





Answers and Solutions

33

It is proved that for all possible numbers i and j elements of matrices (AB)T and

BT AT coincide. In accordance with the deﬁnition of equality of matrices on page [4](#br19)

we get

(AB)T = B A .

T

T

[**1.4**](#br39)[** ](#br39)Solution.

Having calculated the matrix elements by the speciﬁed formulas, we obtain

⎡

⎤

−1 1 −1

⎢

⎥

(1) ⎢ 1 −1 1 ⎥, the sum of all elements S = −1;

⎣

⎡

⎦

−1 1 −1

⎤

1 2 3

⎢

⎥

(2) ⎢2 2 3⎥, S = 22;

⎣

⎡

⎦

⎤

3 3 3

2 1 2

⎢

⎥

(3) ⎢1 0 1⎥, S = 12;

⎣

⎡

⎦

2 1 2

⎤

0

sin 1 sin 2

⎢

⎥

(4) ⎢sin 1

sin 1⎥, S = 4 sin 1 + 2 sin 2.

0

⎣

⎦

sin 2 sin 1

0

[**1.5**](#br40)[** ](#br40)Solution.

(1) For the elements of the third row we have i = 3, j = 1, 2, . . . , n. Therefore,

n

the sum of the elements of the third row is presented in the form

a .

3j

j=1

(2) The elements of the second column may be written as a , where i =

i2

n

1, 2, . . . , n. Then, their sum is equal to

a .

i2

i=1

(3) For the diagonal elements, the indices i and j coincide: a . The sum of squares

ii

n

2

a .

ii

of such elements is

i=1

(4) The secondary diagonal is formed by the elements whose sum of indices is

greater by one to the order of the matrix: i+j = n+1. Therefore, j = (n+1)−i,


n

the module of the sum of these elements is also equal to abs

ai(n+1−i)

.

i=1

[**1.6**](#br40)[** ](#br40)Solution.

Let us write the sum of the elements of the square matrix positioned above the

main diagonal. The number of the elements to be summed up in the rows above





34

1 Matrices and Matrix Algorithms

the main diagonal decreases by one as the row number increases. Due to this,

summation of the elements in the i-th row begins with i + 1, then the sum in one

n

row will be

aij . Performing the summation operation over all rows, we obtain

j=i+1

n n

a .

ij

i=1 j=i+1

Now let us write the sum of the elements positioned below the main diagonal.

The number of the elements to be summed up below the main diagonal increases by

one as the row number increases. Then, the upper summation threshold should be

i−1

equal to i − 1, and the sum for one row is calculated as

aij . For the sum of the

j=1

n i−1

i=1 j=1

elements positioned below the main diagonal, we obtain

a .

ij

[**1.7**](#br40)[** ](#br40)Solution.

By deﬁnition of an antisymmetric matrix, AT = −A, then

⎡

⎤

⎥ ,

⎡

⎢

⎤

0 a21 a31

7

0

−1

0

1

−a14

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

0 a32

a

−a21

−2 −2

⎢

42⎥

⎢

⎥

AT =

−

A

\=

⎢

⎥ .

⎢

⎥

⎢

⎥

−1 2 a33

0

−a31 −a32 −a −a

−7 −a42

33

⎣

⎦

⎣

34⎦

a14 2 a34 a44

0

−a44

Equating the respective matrix elements, we obtain

⎡

⎤

0

1 −1 −7

⎢

⎥

⎢

⎥

−1 0

1 −2 0

7 −2 0

2

2

0

0

⎢

⎥

A = ⎢

⎥ .

⎢

⎥

⎣

⎦

[**1.8**](#br40)[** ](#br40)Solution.

First of all we should note that the number of the elements on the main diagonal

of the matrix is n, while the number of the elements lying above it is n(n − 1)/2.

(1) The elements of the symmetric matrix lying below the main diagonal are

uniquely determined by the upper triangular part of the matrix; this can be

done by 2n(n−1)/2 methods. There exist 2n methods for selection of diagonal

elements. We obtain that the number of symmetric matrices of n rows and n

columns is equal to 2n(n−1)/2 · 2n = 2n(n+1)/2.

(2) The main diagonal of the antisymmetric matrix is ﬁlled with zeros. In order to

determine such a matrix, it is sufﬁcient to specify the elements above the main

diagonal; this can be done by 2n(n−1)/2 methods. Therefore, all in all there exist

2n(n−1)/2 antisymmetric matrices of size n × n.





Answers and Solutions

35

[**1.9**](#br40)[** ](#br40)Solution.

⎡

⎤

⎡

⎤

⎡

⎤

0 0 1

1 1 2

2 2 3

3 3 4

⎡

⎢

⎤

⎥

1 1

3 3

5 5

7 7

5

⎡ ⎤

⎡ ⎤

⎢

⎥

−1 −1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

4

4

15

25

35

⎢

⎥

⎢

⎥

⎢

⎥

a)

⎢ 2 2 ⎥ ⎣ ⎦ =

⎣ ⎦ =

;

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎢

⎥

⎢

⎥

⎢

⎥

1

1

⎣

⎦

⎡

⎣

⎦

⎣

⎦

1

1

⎡

⎤

⎤ ⎡

⎤ ⎡

⎤

⎡

⎤ ⎡

⎤

⎦

3

1 −2

3 −4

1 −2

3 −4

1 −2

3 −4

1 −2

3 −4

−5 6

−9 10

1 −2

3 −4

b) ⎣

⎦ = ⎣

⎦ ⎣

⎦ ⎣

⎦ = ⎣

⎦ ⎣

⎡

⎤

13 −14

21 −22

= ⎣

⎦ .

[**1.10**](#br40)[** ](#br40)Solution.

⎡

⎤ ⎡

⎤

⎡

⎤

0 1 0

0 0 1

0 1 0

⎢

⎥ ⎢

⎥

⎢

⎥

Q1Q2 = 1 0 0

⎢

⎥ ⎢

0 1 0

1 0 0

⎥ = ⎢

0 0 1

1 0 0

⎥;

⎣

⎡

⎦ ⎣

⎤ ⎡

⎦

⎤

⎣

⎡

⎦

⎤

0 0 1

0 0 1

0 1 0

1 0 0

0 0 1

⎤

0 0 1

1 0 0

0 1 0

⎤

⎢

⎥ ⎢

⎥

⎢

⎥

Q2Q1 = 0 1 0

⎢

⎥ ⎢

⎥ = ⎢

⎥;

⎣

⎦ ⎣

⎦

⎣

⎦

1 0 0

⎡

⎤ ⎡

⎡

0 1 0

0 1 0

1 0 0

⎢

⎥ ⎢

⎥

⎢

⎥

2

⎢

⎥ ⎢

⎥

⎢

⎥

Q = 1 0 0

1 0 0

0 0 1

\=

0 1 0 ;

1

⎣

⎡

⎦ ⎣

⎤ ⎡

⎦

⎤

⎣

⎦

0 0 1

0 0 1

⎡

⎤

0 0 1

0 0 1

0 1 0

1 0 0

1 0 0

⎢

⎥ ⎢

⎥

⎢

⎥

2

2

⎢

⎥ ⎢

⎥

⎢

⎥

Q = 0 1 0

\=

0 1 0 .

⎣

⎦ ⎣

⎦

⎣

⎦

⎡

1 0 0

0 0 1

[**1.11**](#br41)[** ](#br41)Solution.

⎤

a b

Let the matrix D have the form ⎣ ⎦, where a, b, c, d are unknown real

c d

numbers.





36

1 Matrices and Matrix Algorithms

Let us square the D and equate the obtained result to the zero matrix.

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

a b

c d

a b

a2 + bc ab bd

\+

0 0

⎣

⎦ ⎣ ⎦ = ⎣

⎦ = ⎣

⎦

.

2

c d

ac + dc bc + d

0 0

Let us write the system of relatively unknown a, b, c, d:

⎧

⎪

2 +

= 0

⎪ a

bc

,

⎪

⎪

⎪

⎨

c(a + d) = 0,

⎪

⎪ b(a + d) = 0,

⎪

⎪

⎪

⎩

a b

bc + d

2 = 0

.

From the obtained system it follows that the matrix D should have the form

⎡

⎤

[⎣](#br41)

⎦, and the variables , and are bound by the condition

a2 + bc = 0.

a b

c

c −a

[**1.12**](#br41)[** ](#br41)Answer:

The size of the matrix L is equal to 1 × 5, the size of the matrix MT is equal to

5 × 1. Therefore, the matrices LMT and MT L have the sizes 1 × 1 (this is a scalar)

and 5 × 5, respectively. Having executed the multiplication operations, we obtain

⎡ ⎤

0

⎢ ⎥

⎢ ⎥

2

⎢ ⎥

⎢ ⎥

LM

T = [−2 −1 0 1 2] ⎢ ⎥ = −2 · 0 + −1 · 2 + 0 · 4 + 1 · 6 + 2 · 8 = 20;

,

, , ,

4

(

)

(

)

⎢ ⎥

⎢ ⎥

⎢6⎥

⎣ ⎦

8

⎡ ⎤

⎡

⎤

0

0

0 0 0 0

⎢ ⎥

⎢

⎥

⎢ ⎥

⎢

⎥

2

−4 −2 0 2 4

−8 −4 0 4 8

⎢ ⎥

⎢

⎥

⎢ ⎥

⎢

⎥

MT L

= ⎢ ⎥ [−2 −1 0 1 2] = ⎢

,

, , ,

⎥

.

4

⎢ ⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢6⎥

⎢−12 −6 0 6 12⎥

⎣ ⎦

⎣

⎦

8

−16 −8 0 8 16

[**1.13**](#br41)[** ](#br41)Answer:

Let H = G2, then

i − j + 1, if i  j,

0, if i < j.

hij

\=





Answers and Solutions

37

[**1.14**](#br41)[** ](#br41)Solution.

⎡

⎤

⎡

⎤

t 0

0 0

Let A = ⎣ ⎦, B = ⎣ ⎦, where t ∈ R.

0 0

t 0

As is easy to see, the equality AB = O is fulﬁlled here, therefore, the product of

two non-zero matrices may be equal to a zero matrix. The student is wrong.

[**1.16**](#br41)[** ](#br41)Solution.

⎡

⎤ ⎡

⎤

cos ψ sin ψ 0

1

0

0

⎢

⎥ ⎢

⎥

A(ψ)B(θ) = − sin ψ cos ψ 0

⎢

⎥ ⎢

0 cos θ sin θ

⎥

⎣

⎡

⎦ ⎣

⎦

0

0

1

0 − sin θ cos θ

⎤

cos ψ sin ψ cos θ sin ψ sin θ

⎢

⎥

= ⎢− sin cos cos cos sin ⎥ .

ψ

ψ

θ

ψ

θ

⎣

⎦

0

− sin θ

cos θ

A(ψ)B(θ)A(ϕ)

⎡

⎣

⎤ ⎡

⎦ ⎣

⎤

cos ψ sin ψ cos θ sin ψ sin θ

− sin cos cos cos sin

cos ϕ sin ϕ 0

⎢

⎥ ⎢

⎥

⎢

⎥ ⎢

⎥

\=

− sin cos

0

⎢

⎥ ⎢

⎥

ψ

ψ

θ

ψ

θ

ϕ

ϕ

⎦

0

− sin θ

cos θ

0

0

1

⎡

⎣

⎤

⎦

cos ψ cos ϕ − sin ψ cos θ sin ϕ cos ψ sin ϕ + sin ψ cos θ cos ϕ sin ψ sin θ

− sin cos − cos cos sin − sin sin + cos cos cos cos sin

⎢

⎥

⎢

⎥

\=

.

⎢

⎥

ψ

ϕ

ψ

θ

ϕ

ψ

ϕ

ψ

θ

ϕ

ψ

θ

sin θ sin ϕ

− sin θ cos ϕ

cos θ

[**1.17**](#br41)[** ](#br41)Solution.

⎡

⎤ ⎡

⎤

⎡

⎤

7 5 3

6 2 3

70 27 44

23 10 18

29 15 50

⎢

⎥ ⎢

⎥

⎢

⎥

AB = 1 3 2

⎢

⎥ ⎢

5 2 1

⎥ = ⎢

⎥,

⎣

⎡

⎦ ⎣

⎤ ⎡

⎦

⎤

⎣

⎡

⎦

⎤

2 2 7

1 1 6

6 2 3

7 5 3

1 3 2

2 2 7

50 42 43

39 33 26

20 20 47

⎢

⎥ ⎢

⎥

⎢

⎥

BA = 5 2 1

⎢

⎥ ⎢

⎥ = ⎢

⎥,

⎣

⎦ ⎣

⎦

⎡

⎣

⎦

1 1 6

⎤

20 −15 1

⎢

⎥

[A, B] = AB − BA = ⎢−16 −23 −8⎥.

[**1.18**](#br41)[** ](#br41)Answer: [A, I] = O.

⎣

⎦

9

−5

3





38

1 Matrices and Matrix Algorithms

[**1.19**](#br41)[** ](#br41)Answer:

[P , P ] = P , [P , P ] = P and [P , P ] = P .

1

2

3

2

3

1

3

1

2

[**1.20**](#br41)[** ](#br41)Solution.

Yes, the equality [A + B, C] = [A, C] + [B, C] is true for any square matrices

A, B and C of the same size. Simple calculations show that

[(A+B), C] = (A+B)C−C(A+B) = AC−CA+BC−CB = [A, C]+[B, C].

[**1.21**](#br42)[** ](#br42)Proof.

Transform the right side of the equality ([1.40](#br42)), relying on the deﬁnition of ([1.20](#br24)):

A[B, C] + [A, C]B = A(BC − CB) + (AC − CA)B.

Then, remove the brackets and indicate the similar summands, following which use

the deﬁnition of the commutator once again:

A[B, C] + [A, C]B = ABC − ACB + ACB − CAB = ABC − CAB = [AB, C].

Thus the identity ([1.40](#br42)) is proved.

[**1.22**](#br42)[** ](#br42)Solution.

No, the equality [A, [B, C]] = [[A, B], C] is fulﬁlled not for all A, B and C, as

the following counterexample shows:

⎡

⎣

⎤

⎦

⎡

⎤

⎦

⎡

⎤

⎦

1 0

0 0

0 1

0 0

1 0

A =

, B

= ⎣

, C

= ⎣

,

0 0

⎡

⎤

⎡

⎤

0 0

1 0

[A, [B, C]] = ⎣ ⎦ , [[A, B], C] = ⎣

Therefore, for the arbitrary matrices [A, [B, C]] = [[A, B], C].

⎦ .

0 0

0 −1

[**1.23**](#br42)[** ](#br42)Answer: the equality is true in the case AB = BA, i.e. if the matrices are

commuting.

[**1.24**](#br42)[** ](#br42)Solution.

This is not true. The following counterexample can be given to the proposition

from the problem situation:

⎡

⎤

⎡

⎤

⎡

⎤

1 0

0 1

1 0

0 1

1 0

A =

⎣

⎦

,

B

= ⎣

⎦

,

C

= ⎣

⎦

.

0 −1





Answers and Solutions

39

In this case, the equalities [A, B] = [A, C] = O are fulﬁlled, while

⎡

⎤ ⎡

⎤

⎡

⎤ ⎡

⎤

⎡

⎤

1 0

0 1

0 1

1 0

0 −2

−2 0

[B, C] = ⎣

⎦ ⎣ ⎦ − ⎣ ⎦ ⎣

⎦ = ⎣

⎦ = O.

0 −1

1 0

1 0

0 −1

Therefore, the matrices B and C are not necessarily commuting.

[**1.25**](#br42)[** ](#br42)Solution.

Calculate the number of multiplication operations for each of the two methods.

(1) During multiplication of each row of the matrix A by each column of the matrix

B, n2 multiplication operations are performed. Since the number of rows is n1,

and the number of columns is n , as a result we obtain n n n operations. The

3

1 2 3

matrix AB has the size n × n ; then for obtaining the matrix ABC from AB

1

3

and C we need n n n operations of multiplication of real numbers. Thus, the

1

3 4

calculation of (AB)C requires n n (n + n ) multiplication operations.

1

3

2

4

(2) Reasoning similarly, we obtain n n (n +n ) multiplication operations required

2

4

1

3

for calculation by the scheme A(BC).

As a result, calculation by the ﬁrst method—as (AB)C—requires less operations

of multiplication of real numbers when fulﬁlling the condition n n (n + n ) <

1

3

2

4

n2n4(n1 + n3).

[**1.30**](#br44)[** ](#br44)Answer: for calculation of the sum of two matrices A and B we will need N2

additions for determining each of N2 elements A + B.

[**1.31**](#br44)[** ](#br44)Solution.

Each of N2 elements of the matrix AB is calculated as a scalar product of two

vectors of size N, which, respectively, requires N additions and N multiplications.

The total number of both additions and multiplications appears to be equal to N ·

2 = 3.

N

N

[**1.32**](#br44)[** ](#br44)Solution.

The cycle body by the variable k may be rewritten in the form

C[i][j] = A[i][0]

B[0][j]

\*

for k in range(1, len(B)):

C[i][j] = C[i][j] + A[i][k]

B[k][j]

\*

Then the number of additions reduces to N3 − N2, while the number of

multiplications remains unchanged.

[**1.33**](#br44)[** ](#br44)Solution.

As is known, the number of multiplication operations required to calculate the

product of matrices of size n × n and n × n equals to n n n . (Recall that

1

2

2

3

1 2 3

the product of two matrices is deﬁned if the number of columns of the ﬁrst one

coincides with the number of rows of the second one.) Due to associativity of





40

1 Matrices and Matrix Algorithms

the multiplication operation, the product A A A can be calculated in two ways:

1

2

3

(A1A2)A3 and A1(A2A3).

In the ﬁrst case, we will need 50·25·30+50·30·10 = 52 500 multiplications and

in the second case— 25 · 30 · 10 + 50 · 25 · 10 = 20 000. So, the minimal number of

multiplication operations required to calculate the elements of the matrix A A A

1

2

3

by the standard algorithm equals to 20 000.

Note There exists an efﬁcient algorithm for ﬁnding the order of multip[licatio](#br420)ns in

the product A A . . . A , n > 2, with the minimal number of operations [[16](#br420)[\].](#br420)

1

2

n

[**1.34**](#br44)[** ](#br44)Answer: 7500.

[**1.35**](#br44)[** ](#br44)Answer: 255,000.

[**1.37**](#br44)[** ](#br44)Solution.

In order to calculate W[i, j] in the rows with numbers 14–15 (see the algorithm

on page [21](#br36)), two logical operations are required. Since this row is executed N ×

3 times, where is the size of the adjacency matrix of the digraph, the

N × N = N

N

full number of operations for obtaining M∗ equals to 2N3.

[**1.38**](#br44)[** ](#br44)Answer:

⎡

⎤

0 1 1 1 1

0 1 1 1 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

M∗ = 0 1 1 1 0

⎢

⎥

.

⎢

⎥

⎢

⎥

⎢0 1 1 1 0⎥

⎣

⎦

0 1 1 1 0

2

N (N + 1)

[**1.40**](#br44)[** ](#br44)Answer: f (N) =

[**1.41**](#br45)[** ](#br45)Answer: g(N) =

.

2

N(N + 1)(2N + 1)

.

6

N(N + 1)(N + 2)(N + 3)

[**1.42**](#br46)[** ](#br46)Answer: h(N) =

[**1.43**](#br46)[** ](#br46)Answer:

.

24

(1) tr A = n(n + 1);

(2) tr A = 0;

n

(3) tr A = n ln 2 + 2 ln(n!), where n! =

i is factorial of the number n;

where k ∈ N;

i=1

3k2,

if n = 2k,

(4) tr A =

3k2 + 3k + 1, if n = 2k + 1,

n 1

(5) tr A = H , where H =

is the n-th harmonic number;

n

n

i

i=1

(6) tr A = 0;





Answers and Solutions

41

1

(7) tr A = − n(n + 2);

2

1

(8) tr A = n(n + 1) + H , where H is harmonic number (see above).

n

n

2

[**1.44**](#br46)[** ](#br46)Proof.

The trueness of the statement tr (AB) = tr (BA) follows from the chain of

equalities:



i↔j

tr (AB) =

a b

ij ji

\=

b a

ji ij

\=

b a = tr (BA).

ij ji

i,j

i,j

i,j





**Chapter 2**

**Matrix Algebra**

**2.1 Determinant of a Matrix: Determinants of the Second**

**and Third Order**

One of the fundamental notions of linear algebra is the **determinant of a square**

**matrix**. Let us begin considering this notion with the determinants of the second

and third order.

⎡

⎤

a11 a12

a21 a22

We will associate the matrix A = ⎣

⎦ of size 2 × 2 with the number

a11a22 − a21a12,

(2.1)

which is called the **second order determinant** of the matrix A and is denoted as






a11 a12

` `≡ det A ≡ |A| ≡


.

(2.2)


a a 

21 22

⎡

⎤




3 2

3 2

Example 2.1 If A = ⎣ ⎦, then  =   = 3 · 5 − 1 · 2 = 13.



1 5

1 5

© Springer Nature Switzerland AG 2021

43

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_2>





44

2 Matrix Algebra

**Third order determinant** of the matrix A of size 3 × 3 is a number obtained by

the following formula:




a11 a12 a13


` `≡ det A ≡ |A| ≡ a


` `21 22 23

a

a




a31 a32 a33

= a a a + a a a + a a a

11 22 33

12 23 31

13 21 32

−a a a − a a a − a a a .

(2.3)

13 22 31

12 21 33

11 23 32

The formula ([2.3](#br58)) can be easily remembered with the help of the **triangle rule**:

the value of the third order determinant is equal to the algebraic sum of six terms,

each being a product of three elements, one from each row and each column of the

matrix A. The sign “+” is taken by the product of the elements lying on the main

diagonal, and two products of the elements forming within the matrix triangles with

bases parallel to the main diagonal. The sign “−” is taken by the products of the

elements lying on the secondary diagonal, and two products of the elements forming

triangles with bases parallel to the secondary diagonal (see Fig. [2.1](#br58)). Unfortunately,

triangle rule is only applicable to calculation of the determinants of matrices of

size 3 × 3. The next Sect. [2.2](#br59)[ ](#br59)describes what to do with the matrices of greater

size.

**Fig. 2.1** The scheme “triangle rule” for calculation of the third order determinant





2.2 Determinants of the n-th order: Minors

45

Example 2.2





4

2 2




det A = |A| = −4 −3 1



` `3 0 3

= 4 · (−3) · 3 + 2 · 1 · 3 + 2 · (−4) · 0

− 2 · (−3) · 3 − 2 · (−4) · 3 − 4 · 1 · 0

= −36 + 6 + 0 + 18 + 24 − 0 = 12.

Note that the ﬁrst order determinant for the matrix A = [a ], consisting of one

11

element, is equal to the value of this element: det[a ] = a .

11

11

**2.2 Determinants of the n-th order: Minors**

The determinant of the n-th order, where n  2, has the form




a11 a12 . . . a1 

n




a21 a22 . . . a2

n

` `= 

(2.4)

` `.

.

.

.

.

` `.

.

.

. 

` `.

.

.

. 




a 1 a 2 . . . a

n

n

nn

By analogy with ([2.3](#br58)) it is a polynomial each summand of which is a product of

exactly n elements of the matrix (aij ), and only one multiplier is included into the

product from each row and each column of this matrix.

Now let us turn to strict deﬁnitions.

Let the ordered set of indices (k , k , . . . , k ) form some permutation of the

1

2

n

numbers 1, 2, . . . , n. For n ﬁrst natural numbers, as is easy to see, there exist n!

pairwise different permutations.

**Inversion in permutation** or simply **inversion** is the pair (k , k ), where the

1

2

greater number stands before the smaller one: k > k .

1

2

Example 2.3 In the collection (4, 3, 2, 1) there are six inversions: (4, 3), (4, 2),

(4, 1), (3, 2), (3, 1), (2, 1); there are no other inversions in this collection.

Note The only permutation that contains no inversion is the identity permutation

(1, 2, . . ., n).





46

2

Matrix Algebra

**Determinant** of the n-th order of the matrix (aij ) is the sum

det A =

(−1)σ a1k1 a2k2 . . . ankn

,

(2.5)

perm

where summation is performed over all permutations, σ is the number of inversions

in the permutation (k , k , . . . , k ). The determinant contains n! terms, half of which

1

2

n

is taken with a positive sign and half with a negative sign.

Example 2.4 Let us expand the deﬁnition ([2.5](#br60)) for the case n = 2.

**Solution** For n = 2 we have 2! = 1 · 2 = 2 permutations, namely k = 1, k = 2

1

2

and k = 2, k = 1. The sum in det A will consist of two terms: a a and a a ,

1

2

11 22

12 21

taken with positive and negative signs, respectively:

0

1

det A =

(−1)σ a1k1 a2k2 = (−1) a a + (−1) a a .

(2.6)

11 22

12 21

perm

The obtained formula exactly correlates with the deﬁnition ([2.1](#br57)), provided in

Sect. [2.1](#br57).

If we remove from the matrix A of the n-th order the i-th row and the j-th

column, then we will obtain the matrix of the (n−1)-th order, whose determinant is

called the **complementary minor of the element** a of the matrix A and is denoted

ij

by Mij .

The variable Aij = (−1)i+j M is called the **algebraic complement** (**cofactor**)

ij

of the element aij of the matrix A.

Example 2.5 Given the determinant





2

1 −2




` `= 3 −1 4


,

(2.7)



−3 5 0 

then the complementary minors of the elements of the matrix a and a31 and their

23

cofactors are equal to




` `2 1

M23 =

` `= 10+3 = 13

, A23

= −1 2+3

(

)

M23

= −1 ·13 = −13

(

)

,

(2.8)


−3 5




` `1 −2

M31 =

` `= 4 − 2 = 2

, A31

= −1 3+1

(

)

M31

= 2

.

(2.9)


−1 4 






2.2 Determinants of the n-th order: Minors

47

**Theorem 2.1 (Laplace[**1](#br61))** For the determinant of the matrix A = (a ) the follow-

ij

ing formulas are true:

n

j=1

det A =

det A =

aij Aij , i = 1, 2, . . . , n,

(2.10)

(2.11)

n

i=1

aij Aij , j = 1, 2, . . . , n,

i.e. the determinant can be expanded over any row or any column, using the

cofactors of the matrix elements.

The formulas ([2.10](#br61)) and ([2.11](#br61)) allow reducing the calculation of the determinant

of the n-th order to calculation of the determinant of the (n − 1)-th order. The

procedure of reduction of order continues until we arrive at the determinants of

the second and third order, which are relatively easy to calculate.

Relations ([2.10](#br61)) and ([2.11](#br61)) are referred to as the **Laplace expansions**.

Example 2.6 Let us calculate the determinant of the fourth order, expanding it in

the ﬁrst column:




2 3 −3 4

2 1 −1 2



















1 −1 2

3 −3 4

3 −3 4

1 −1 2
















` `= 

` `= 2 2 1

0

` `− 2 

2 1

0

` `+ 6 







6 2 1

0





3 0 −5

3 0 −5

3 0 −5


2 3 0 −5




3 −3 4




− 2 1 −1 2 = 2(−5 + 0 + 0 − 6 − 0 − 10)

− 2(−15 + 0 + 0 − 12 − 0 − 30) + 6(15 − 18 + 0 + 12 − 0 − 15)

− 2(0 − 12 + 4 + 8 − 6 − 0) = −42 + 114 − 36 + 12 = 48.




2 1 0

1Pierre-Simon, marquis de Laplace (1749–1827), French mathematician, physicist and astronomer.





48

2 Matrix Algebra

**2.3 General Properties of Determinants: Elementary**

**Transformations of a Matrix**

Let us enumerate the general properties of determinants [\[](#br421)[43](#br421)[,](#br421)[ ](#br421)[63](#br422)[\].](#br422)

**Property 1** During transposition of a matrix, its determinant does not change:

det AT = det A.

(2.12)

**Property 2** After exchange of two rows (columns) of a matrix, the determinant

changes its sign.

**Property 3** The determinant of a matrix with two identical rows (columns) is equal

to zero.

**Property 4** The determinant of a matrix with two proportional rows (columns) is

equal to zero.

**Property 5** The determinant of a matrix will not change if to all elements of its row

(column) are added the respective elements of another row (column), multiplied by

the same number.

**Property 6** The determinant of a product of matrices is equal to the product of

determinants, i.e.

det(A · B) = det A · det B.

(2.13)

**Property 7** The determinant of a triangular matrix coincides with the product of

the elements standing on the main diagonal.

**Property 8** If all the elements of some row (column) of a matrix are multiplied by

the same number, its determinant will be multiplied by this number.

**Property 9** If all the elements of the i-th row of a determinant are given as a sum

of two terms aij = u + v for j = 1, . . . , n, then the determinant is equal to the

j

j

sum of two determinants of the following form:













a11

a12 . . . a1n

a a12 . . . a1n

a a12 . . . a1n

11

11












. . . . . . . . . . . . . . . . . . . . . . . . .

. . . . . . . . . . . . . .

. . . . . . . . . . . . . .













` `= 

` `+ 

\+ v u + v . . . u + v

.

u1

1

2

2


u1 u2 . . . un


v1 v2 . . . vn

n

n






` `. . . . . . . . . . . . . . . . . . . . . . . . .   . . . . . . . . . . . . . .   . . . . . . . . . . . . . . 


















a 1

n

a 2 . . .

n

a

a 1 a 2 . . . a

a 1 a 2 . . . a

n n nn

nn

n

n

nn

(2.14)

**Property 10** If all the elements of some row or column of a matrix are equal to

zero, then its determinant is equal to zero.





2.3 General Properties of Determinants: Elementary Transformations of a Matrix

49

**Elementary transformations** of a matrix are such transformations that are

associated with Properties 2, 5, 8: exchange of two rows (columns); multiplication

of a row (column) by a non-zero number; addition to one of the matrix row of

another one, multiplied by any non-zero number (the same for the columns).

With the help of the elementary transformations, the matrix may be reduced to a

triangular form, while its determinant may then be easily obtained using Property 7.

Example 2.7 Calculate the determinant




2 3 −3 4

2 1 −1 2








(2.15)




6 2 1

0




2 3 0 −5

using the elementary transformations of the matrix corresponding to this determi-

nant.

**Solution**

(1) We subtract from the second and fourth rows the ﬁrst row, and from the third

row—the ﬁrst row multiplied by 3.

As a result we obtain








2 3 −3 4

2 1 −1 2

2 3 −3

4












0 −2 2 −2

0 −7 10 −12




\=

;

(2.16)








6 2 1

0








2 3 0 −5 0 0

3

−9 

7

(2) add to the third row the second row multiplied by − :

2




2 3 −3 4

0 −2 2 −2

0 0 3 −5








;

(2.17)








0 0 3 −9

(3) subtract from the fourth row the third row:




2 3 −3 4

0 −2 2 −2

0 0 3 −5








(2.18)

` `.






0 0 0 −4





50

2 Matrix Algebra

As a result we obtain the determinant of the upper triangular matrix, which is

equal to the product of the elements positioned on the main diagonal:

2 · (−2) · 3 · (−4) = 48.

(2.19)

Note Note that linear algebra knows [alternat](#br422)ive methods to ﬁnd the variable det A,

in particular, the axiomatic deﬁnition [[63](#br422)[\].](#br422)

**2.4 Inverse Matrix**

Let A be a square matrix of size n × n, and I is an identity matrix of the same size.

The matrix B is called the **inverse** of the matrix A, if the following equalities are

fulﬁlled

A · B = B · A = I.

The matrix inverse of A is denoted as A−1.

Note that the inverse matrix exists not for every matrix.

**Theorem 2.2** If the determinant of the matrix A is equal to zero, i.e. det A = 0,

−1

then the inverse matrix of A does not exist.

A square matrix is referred to as **nonsingular** (or **nondegenerate**), if an inverse

matrix is determined for it. Otherwise, A is a **singular** (**degenerate**) matrix. It is

known that the matrix inverse of the nonsingular matrix is the only one.

**Theorem 2.3** If the determinant of the matrix A = (a ) is other than zero, i.e.

ij

` `= det A = 0, then the inverse matrix exists:

1 

A−1

\=

Aij

T

,

(2.20)

where (Aij ) is a matrix formed by cofactors of the elements aij of the matrix A

(cofactor matrix).

Note A matrix t[ranspos](#br420)[ed](#br421)[ ](#br421)t[o](#br422)[ ](#br422)[(A](#br422)[ij](#br422)[ ](#br422)[)](#br422)[ ](#br422)is called **adjugate**, or **classical adjoint**, relative

to the original one [[15](#br420)[,](#br420)[ ](#br420)[35](#br421)[,](#br421)[ ](#br421)[64](#br422)[,](#br422)[ ](#br422)[65](#br422)[\].](#br422)

The following statements are true:

\1. If the matrix A is invertible, then AT is also invertible, and (AT )−1 = (A−1)T .

\2. If the matrices A and B are invertible, then (A B)−1 = B−1 A−1.





2.4 Inverse Matrix

51

\3. The matrix inverse of the upper (lower) triangular matrix is also the upper (lower)

triangular one.

1

\4. If A−1 exists, then det(A−1) =

.

det A

Example 2.8 Find the inverse matrix of the matrix:

⎡

⎤

2 5

7

4

⎢

⎥

A = 6 3

⎢

⎥

.

(2.21)

⎣

⎦

5 −2 −3

**Solution** The determinant of the matrix is equal to












` `3 4 

6 4 

6 3 

det A = 2 

` `− 5 

` `+ 7 







−2 −3

5 −3

5 −2

= 2(−9 + 8) − 5(−18 − 20) + 7(−12 − 15) = −1.

(2.22)

(2.23)

Calculate the cofactors:








` `3 4 

6 4 

A11 = (−1)1+1 

= −1, A12 = (−1)

1+2 

= 38,




−2 −3

5 −3








6 3 

` `5 7 

A13 = (−1)1+3 

= −27, A21 = (−1)

= −41, A23 = (−1)

2+1 

= 1,

(2.24)

(2.25)

(2.26)

(2.27)




5 −2

−2 −3








2 7 

2 5 

A22 = (−1)2+2 

2+3 

= 29,




5 −3

5 −2








5 7

2 7

A31 = (−1)3+1 

= −1, A32 = (−1)

3+2 

= 34,




3 4

6 4




2 5

A33 = (−1)3+3 

= −24.


6 3





52

2

Matrix Algebra

Write the matrix formed by the cofactors:

⎡

⎤

−1 38 −27

⎢

⎥

⎢

⎥

(2.28)

1 −41 29

.

⎣

⎦

−1 34 −24

As a result, the desired inverse matrix will have the form:

⎡

⎤

⎡

⎤

−1

1

−1

1

−1

1

1

⎢

⎥

⎢

⎥

A−1

\=

⎢

⎥

\=

⎢

⎥

.

(2.29)

38 −41 34

−38 41 −34

27 −29 24

⎣

⎦

⎣

⎦

(−1)

−27 29 −24

**2.5 Integer Powers of a Matrix**

The notion of raising a number to an integer power in matrix algebra is easily

generalized. By deﬁnition we have

A0 = I, A1 = A, A2 = AA, A3 = AAA, . . . ,

(2.30)

and if A is a nondegenerate matrix, then

A−p = (A−1)p = (A )

p −1

.

(2.31)

For diagonal matrices, their p-th power preserves the property of diagonality:

⎡

⎤

⎡

⎤

p

d1 0 . . . 0

d

p 0

. . .

0

1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 d2 . . . 0

0 d2p . . . 0

⎢

⎥

⎢

⎥

\=

(2.32)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

. . . . . . . . . . . .

. . . . . . . . . . . .

⎣

⎦

⎣

⎦

0 0 . . . dn

0 0 . . . dnp

for all integer p.

In order to solve the following problems, we will need the mathematical

induction method.





2.5 Integer Powers of a Matrix

53

**2.5.1 Mathematical Induction Method**

For proving the statements depending on a nat[ural](#br420)[ ](#br420)[paramet](#br420)er, mathematics widely

uses the **mathematical induction method** [[1](#br420)[,](#br420)[ ](#br420)[17](#br420)[,](#br420)[ ](#br420)[66](#br422)[\]](#br422)[ ](#br422)(from Latin inductio—

derivation).

**Mathematical Induction Principle** Let P (n) be a statement deﬁned for all natural

numbers n, and let the following conditions be fulﬁlled:

(1) P(1) is true;

(2) ∀k  1 the logical implication is true P (k) ⇒ P (k + 1) .

Then P (n) is true for any natural n.

The proposition 1 is usually referred to as the **basis step**, and the proposition

2—**inductive step**.

In order to prove identities by the mathematical induction method, the following

is done. Let the statement P (k) take the true value when the considered identity is

true for some natural number k. Then, two statements are proved:

(1) basis step, i.e. P(1);

(2) inductive step, i.e. P (k) ⇒ P (k + 1) for an arbitrary k  1.

According to the mathematical induction method, a conclusion is made about

trueness of the considered identity for all natural values of n.

Note that in mathematical logic a statement of the form P (n) is called **predicate**.

Example 2.9 Using the mathematical induction method, we will prove the state-

ment:

1 + 3 + 5 + · · · + (2n − 1) = n2 for all natural numbers n.

**Proof** Let P (n) be the predicate “1 + 3 + 5 + · · · + (2n − 1) = n2”.

B a s i s s t e p

For n = 1 we obtain 1 = 12, i. e. P(1) is true.

I n d u c t i v e s t e p

Assume that for n = k the statement 1 + 3 + 5 + · · · + (2k − 1) = k2 is true.

Prove the trueness of P(k + 1):

1 + 3 + 5 + · · · + (2k − 1) + (2(k + 1) − 1)

= k + (2(k + 1) − 1) = k + 2k + 1 = (k + 1) .

2

2

2

Thus, for any natural k the implication P (k) ⇒ P (k + 1) is true. Then, by

the principle of mathematical induction the predicate P (n) has a true value for all

natural n.

Example 2.10 Relying on the mathematical induction method, prove that n2 +

even for all natural n.

n

is





54

2 Matrix Algebra

**Proof** Denote f (n) = n2 + n and P (n)—the predicate “f (n) is divisible by 2”.

B a s i s s t e p

2

For n = 1 we obtain f (1) = 1 + 1 = 2—even number, this is why P(1) is true.

I n d u c t i v e s t e p

Assume that f (k) is even for natural k  1. Let us prove that it implies evenness

of f (k + 1):

2

2

f (k + 1) = (k + 1) + (k + 1) = k + 2k + 1 + k + 1

2

= (k + k) + 2k + 2 = f (k) + 2(k + 1).

Since in the right side of the obtained relation stands the sum of two even numbers,

then f (k + 1) is divisible by 2.

Note The statement of the example becomes apparent if we represent the expression

k

2 + in the form 2 +

k

k

k

\=

k(k

\+ 1 . Out of two consecutive natural numbers, one

)

is necessarily even, and their product is divisible by two.

⎡

⎤

a c

Example 2.11 Calculate the hundredth power of the matrix A = ⎣ ⎦.

0 a

Let us ﬁnd several lower powers of this matrix:

⎡

⎤

⎡

⎤ ⎡

⎤

⎡

⎤

⎦

⎡

⎣

⎤

⎦

a c

a c

a c

a2 2ac

a

3 3 2

a c

A1 =

⎣

⎦

, A2 =

⎣

⎦ ⎣

⎦

\=

⎣

, A3 =

, . . .

(2.33)

0 a

0 a

0 a

0 a2

0

a3

An assumption arises that for all natural values of n the following equality is true:

⎡

⎤

⎡

⎤

n

a c

an nan−1

c

⎣

⎦ = ⎣

⎦.

0 a

0

an

In order to verify this assumption, let us use the mathematical induction method.

Prove that for all natural n the equality is fulﬁlled:

⎡

⎤

⎦

an nan−1

c

A

n = ⎣

.

(2.34)

0

an

⎡

⎤

an nan−1

c

**Proof** Denote the predicate “An = ⎣

⎦” through P (n).

0

an

B a s i s s t e p

Consider the case n = 1. The equality takes the form A1 = A, which is the true

statement.

I n d u c t i v e s t e p





2.5 Integer Powers of a Matrix

55

Assume that P (k) for some k = 1, 2, . . . takes the true value, i.e. Ak =

⎡

⎣

⎤

k

k−1

a ka

c

⎦. Prove that

\+ 1 is true.

P(k

)

0

ak

Write the predicate P(k + 1) in the form:

⎡

⎤

⎦

ak+1 (k

\+ 1

)akc

Ak+1 = ⎣

.

(2.35)

0

ak+1

Let us use the inductive supposition and rewrite the sum Ak+1 as AkA:

⎡

⎤ ⎡

⎤

⎡

⎤

ak kak−1

c

a c

a

k ·

0

a a c ka c a

k + k−1 ·

k+1 = ⎣

⎦ ⎣ ⎦ = ⎣

⎦

.

A

0

ak

0 a

ak · a

After algebraic transformations we obtain

⎡

⎤

ak+1 (k

\+ 1

)akc

Ak+1 = [⎣](#br69)

⎦

.

+1

ak

0

This expression coincides with ([2.35](#br69)). Then, for any k = 1, 2, . . . the implication

P (k) ⇒ P(k + 1) is true, and the mathematical induction method has proved that

⎡

⎤

n

a na

n−1

c

A

n = ⎣

⎦ for all natural .

n

0

an

Substituting in ([2.34](#br68)) the value n

\=

100, we ﬁnally obtain A100

\=

⎡

⎣

⎤

a

100 100 99

a c

⎦.

0

a100

The operation of raising the matrix to power can be executed by a relatively small

number of calculations, if the original matrix is presentable in the form

B = U−1DU,

(2.36)

where D is a diagonal matrix, U is a nonsingular matrix: UU−1 = I. We will carry

of the calculation of Bp = (U−1DU)p relying on the associativity property of the

multiplication operation (see page [8](#br23)):

Bp = (U−1DU)p = (U−1DU)(U−1DU)(U−1DU) . . . (U−1DU)(U−1DU)



!

p times

= U−1D(UU−1)D(UU−1)D(U . . . U−1)D(UU−1)DU

= U−1DIDID . . . DIDU = U−1 (DD . . . D) U = U−1DpU.

(2.37)



!

p times





56

2 Matrix Algebra

The rule of raising the matrix B to power is generalized in case of integer negative

p = −abs(p):

B−abs(p) = (U−1BU)−abs(p) = ((U−1BU)

−1 abs(p)

)

= (U−1B−1(U

−1 −1 abs(p)

)

)

= (U−1B−1U)abs(p)

= U−1B−abs(p)U = Bp.

(2.38)

Therefore, the above reasoning proves the theorem of raising to an integer power

of matrices B of a special form ([2.36](#br69)).

**Theorem 2.4 (Matrix Power Theorem)** Fo r an arbitrary matrix B, presentable

in the form B = U−1DU, and the integer number p the following equality is true:

Bp = U−1DpU.

(2.39)

Example 2.12 Prove that various integer powers of the matrix commute

p1 p2 = p2 p1

(2.40)

A A

A A

**Proof** Indeed, based on the properties of the operation of raising to power, we have

p1 p2 =

A A

Ap1+p2 = Ap2+p1 = A A

p2 p1 .

**2.6 Functions of Matrices**

A matrix may act as an argument of some function. Let us begin with consideration

of a polynomial of a matrix. As is known, a polynomial of degree p in variable x is

the sum f (x) of the form:

2

p

f (x) = c0 + c1x + c2x + · · · + c x ,

(2.41)

p

where c (i = 0, 1, . . . , p) are arbitrary numerical coefﬁcients.

i

By the **polynomial** f (A) of degree p of the matrix A we will understand the

following expression:

2

p

f (A) = c0I + c1A + c2A + · · · + c A .

(2.42)

p

As is easy to see, the value of the function f (A) is, in its turn, some matrix as

well. Its elements are expressed by the formulas:

(f (A))ij = c0δij + c1(A)ij + c2(A2) + · · · + c (A ) .

(2.43)

p

ij

p

ij





2.6 Functions of Matrices

57

Using the theorem about the power of a matrix of the special form ([2.39](#br70)), we will

write the relation

f (U−1AU) = U−1f (A)U,

(2.44)

which is true for an arbitrary orthogonal matrix U.

**Fractionally rational function** of a matrix is the value

f1(A)

= f (A)(f (A)) = (f2(A))−1f1(A)

−1

(2.45)

1

2

f2(A)

if det f (A) = 0.

2

Let us demonstrate the correctness of the introduced deﬁnition, i.e. that two

products in ([2.45](#br71)) are always equal to each other. Indeed, having multiplied both

parts of the equality f (A)(f (A))−1 = (f (A))−1f (A) by f (A) on the right and

1

2

2

1

2

then by f (A) on the left, we obtain

2

f2(A)f1(A) = f1(A)f2(A).

(2.46)

The polynomials f (A) and f (A) depend only on the matrix A, and, therefore,

1

2

f1(A)

f2(A)

commute. Due to this, the fraction

is deﬁned correctly [[53](#br422)[\].](#br422)

**2.6.1 Exponent and Logarithm**

The inﬁnite sum of the matrices of size m × n of the form

A + B + C + · · · + Z + · · ·

(2.47)

is called a **series**. It is said that the series **converges**, if for all i = 1, 2, . . ., m

and j = 1[,](#br422)[ ](#br422)[2](#br422)[,](#br422)[ ](#br422). . . , n converge the sequences of the respective components of these

matrices [[53](#br422)[\]:](#br422)

aij + bij + · · · + tij + · · ·

(2.48)

By deﬁnition, the **exponent** eA of the square matrix A is set equal to the sum

1

1

1

eA =

I

\+

A

\+

A2 + A3 + · · · + Ap + · · ·

(2.49)

2!

3!

p!

It is known that this series converges for any real square matrix [[37](#br421)[\].](#br421)[ ](#br421)The matrix I

in the formula ([2.49](#br71)) is taken of the same order as A.





58

2

Matrix Algebra

In a compact form, this sum can be presented as

∞

Ap

eA =

.

(2.50)

p!

p=0

Sometimes, especially when writing formulas with fractions, another notation for

the matrix exponent is used, namely exp A.

⎡

⎤

1 λ

Example 2.13 Calculate exp ⎣ ⎦ , where λ ∈ R.

0 1

**Solution** As follows from the formula ([2.34](#br68)) in Example [2.11](#br68), for all natural p the

⎡

⎤

⎡

⎤

⎡

[⎤](#br68)

p

1 λ

1 pλ

1 λ

equality is fulﬁlled ⎣ [⎦](#br71)[ ](#br71)= ⎣

⎦. Denote A = ⎣ ⎦ .

0 1

0 1

0 1

Using the deﬁnition ([2.49](#br71)), we obtain

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

∞

Ap

1 0

1

1

1 2

1

1 3

λ

λ

λ

eA =

= ⎣ ⎦ + ⎣ ⎦ +

⎣

⎦ +

⎣

⎦ +

. . .

p!

2! 0 1

3! 0 1

0 1

0 1

p=0

⎡

⎤

∞

1

∞

⎡

⎤

p

⎡

⎤

⎡

⎤

∞

1

λ

⎢

!

!⎥

e λ

1

λ

p

p

⎢

⎥

e λe

=0

p=0

− 1 !

= ⎢p

⎥ =

(p

e

)

= ⎣

⎦ = e ⎣ ⎦ .

⎣

p=1

⎦

⎣

∞ 1 ⎦

0 e

0 1

0

0

p!

p=0

(2.51)

During calculation of the elements of the matrix eA we used the deﬁnition of the

number e = 2.71818 . . . (also known as, **ba[ses**](#br422)[ ](#br422)of the natural logarithms**), known

from the course the mathematical analysis [[76](#br422)[\]:](#br422)

∞

` `1

1

1

1

e =

= 1 +

\+

\+ · · · +

\+ · · ·

(2.52)

p!

1! 2!

p!

p=0

Note The notion of t[he](#br420)[ ](#br420)[mat](#br420)rix exponent is widely used in the theory of systems of

differential equations [\[](#br420)[3](#br420)[\].](#br420)

**Logarithm** of the square matrix A is the sum

1

1

1

2

3

p−1

ln A = (A−I)− (A−I) + (A−I) −· · ·+(−1)

(A−I)p+· · · , (2.53)

2

3

p





2.7 Matrix Rank

59

if this series converges. As in the case with the matrix exponent, the identity matrix

I in the formula ([2.53](#br72)) must have the same order as A. In a compact form, the

sum ([2.53](#br72)) can be presented as follows:

∞

` `−1 p

(

)

ln A =

(A − I)p.

p

p=1

⎡

⎤

1 λ

Example 2.14 Calculate ln ⎣ ⎦ , where λ ∈ R.

0 1

**Solution** We will need the natural powers of the difference of the matrices (A −

⎡

⎤

0 λ

I) =

⎣

⎦.

0 0

⎡

⎤ ⎡

⎤

⎡

⎤

0 λ

0 λ

0 0

Since (A − I)2 = ⎣ ⎦ ⎣ ⎦ = ⎣ ⎦, then all the summands of the series

0 0

0 0

0 0

in ([2.53](#br72)), except the ﬁrst one, are in this case equal to the zero matrix. Therefore,

⎡

⎤

0 λ

the value ln A is fully deﬁned by the ﬁrst summand of the series ln A = ⎣ ⎦. 

0 0

**Theorem 2.5** For the determinant of an arbitrary matrix A, the formula

det A = exp(tr ln A)

(2.54)

is valid.

Note Many examples of usi[ng](#br421)[ ](#br421)various functions of matrices for solving practical

problems are considered in [[34](#br421)[\].](#br421)

**2.7 Matrix Rank**

**Minor** of the k-th order Mi1,i2,...,ik of the matrix A of size m × n is the determinant

j1,j2,...,j

k

of the matrix obtained from the elements, standing at the intersection of the

selected rows with numbers i , i , . . . , i and columns with numbers j , j , . . . , j

1

2

k

1

2

k

on condition that 1  i < i < · · · < i  m and 1  j < j < · · · < j  m.

1

2

k

1

2

k

Example 2.15 Given the square matrix

⎡

⎤

a11 a12 a13

⎢

⎥

A =

⎢

⎥

,

(2.55)

⎣ 21

a

a22

a

23⎦

a31 a32 a33





60

2 Matrix Algebra

for which the number of rows m and the number of columns n are equal to m =

n = 3.

Then the second order minors of the matrix A have the form












a11 a12

a11 a13

1,2

1,2


1,2

1,3


M

\=

,

M

\=

,

(2.56)

(2.57)




a a 

a a 

21 22

21 23












a11 a12

a11 a13

1,3

1,2


1,3


M

\=

,

M

\=


1,3


a a 

a a 

31 32

31 33

and so on until the minor






a22 a23

2,3

2,3


M

\=

.

(2.58)


a a 

32 33

All in all, for the matrix of size 3 × 3 nine second order minors can be formed

(the number of arbitrary order matrix minors see in solution of Problem [**2.18**](#br82)).

The number r is called the **rank** of the matrix A, if there exists a minor of order

r, other than zero, and all minors of greater order are equal to zero.

Any minor of maximal order r, other than zero, is referred to as **basic minor**.

For the rank of the matrix A the designation rk A is used.

In the following presentation, we need the concept of linear dependence of the

matrix rows. Let us give k rows of the form

U1 = [u11 u12 . . . u1n],

U2 = [u21 u22 . . . u2 ],

n

(2.59)

. . . . . . . . . . . . . . . . . . . . .

U = [u 1 u 2 . . . u ],

k

k

k

kn

each of which contains n real numbers.

We multiply every element of the ﬁrst row by real number α1, every element of

the second row multiply by α1, etc. Then we add corresponding elements of rows.

As a result, a new row W forms

W = α1U1 + α2U2 + · · · + αkuk

= α1[u11 u12 . . . u1n]

\+ α2[u21 u22 . . . u2n]

........................

\+ αk[uk1 uk2 . . . ukn].

(2.60)





2.7 Matrix Rank

61

The row W is called a **linear combination** of rows U (i = 1, 2, . . . , k). The

numbers α , where i = 1, 2, . . ., k, are said to be the **coefﬁcients of a linear**

i

**combination** of rows.

If there is a collection of real numbers α , α , . . . , α , among which at least one

1

2

k

is not equal to zero, such that W is the zero row, then U , U , . . . , U are called

1

2

k

**linearly dependent**. Otherwise, these rows are said to be **linearly independent**.

Similarly, the deﬁnition of linear dependence/independenceof matrix columns is

introduced.

Example 2.16 The rows U1 = [1 0 −3], U2 = [3 −2 1], U3 = [5 −2 −5] are

linearly dependent, since there is a linear combination of them equal to the zero

row:

2U + U − U = [0 0 0].

(2.61)

1

2

3

**Theorem 2.6 (Basic Minor Theorem)** The number of linearly independent rows

and columns of a matrix is the same and equals to the order of the basic minor. And

the rows (columns), included into the basic minor, are linearly independent, and the

rest are linearly expressed through them.

Note A zero matrix has no linearly independent rows. This is why the rank of the

[matr](#br421)[ix](#br421)[ ](#br421)formed by zero elements will be considered as equal to zero by deﬁnition

[[36](#br421)[,](#br421)[ ](#br421)[47](#br421)[\].](#br421)

The elementary transformations do not change the rank of a matrix.

Recall that the **elementary transformations** of a matrix are (see Sect. [2.3](#br62)):

(a) exchange of two rows (columns);

(b) multiplication of a row (column) by a non-zero number;

(c) addition to one of the matrix row of another one, multiplied by any non-zero

number (the same for the columns).

When calculating the rank of the matrix, deletion of a zero row (column) or one

of the two proportional rows (columns) is used, it does not change the rank of the

matrix.

The matrix is referred to as **echelon matrix**, if each its row begins with a strictly

greater number of zeroes, than the previous row.

One of the basic methods of ﬁnding the rank of the matrix is the method of

elementary transformations.

**Elementary transformations method** allows bringing the matrices to the

echelon form with the help of the following algorithm:

(1) Select the row at the beginning of which stands a non-zero element. This row is

written ﬁrst and is called the **pivot row**.





62

2

Matrix Algebra

(2) To all the remaining rows the pivot row is added, multiplied by

ai1

−

(2.62)

a11

(here i is the number of the row to which the pivot row is added). As a result, in

all rows except the pivot one the ﬁrst elements will be equal to zero.

(3) Out of the remaining rows the one is selected whose second element is not equal

to zero. It is written second and is considered to be the pivot one.

(4) To the remaining rows the pivot row is added, multiplied by

ai2

−

.

(2.63)

a22

As a result in the second column the zero elements have formed, except the ﬁrst

and the second rows.

This process continues until obtaining the echelon matrix. The number of non-

zero rows in this matrix will be its rank.

Example 2.17 Find the rank of the matrix using the method of elementary transfor-

mations:

⎡

⎤

3 5 7

⎢

⎥

A = 1 2 3

⎢

⎥

.

(2.64)

⎣

⎦

1 3 5

The third order minor is the determinant of the matrix: M1,2,3 = det A.

1,2,3

Calculate the determinant of the matrix A by the ﬁrst column expansion method:












2 3

5 7

5 7

det A = 3 · (−1)1+1 

\+ 1 · (−1)

2+1 

\+ 1 · (−1)

3+1 







3 5

3 5

2 3

= 3 · (10 − 9) − 1 · (25 − 21) + 1 · (15 − 14) = 3 − 4 + 1 = 0.

Consider the second order minor




3 5

1,2

1,2


M

\=

= 1 = 0.

(2.65)


1 2

Since it is not equal to zero, then rk A = 2.

It is often difﬁcult to calculate the matrix rank based on its deﬁnition because one

has to search through a great number of minors. As a rule, in order to simplify the





2.7 Matrix Rank

63

calculation of the matrix rank, it is reduced to a simpler form using the elementary

transformations (see Sect. [2.3](#br62)).

So, the rank of the matrix presented in the echelon form is equal to the number

of the non-zero rows.

In what follows, we will use the following designations for the equivalent

transformations:

• A → B—the matrix B is obtained as a result of the elementary transformation

of the matrix A;

• (i) + a(j)—addition to the i-th row of the matrix of the row with number j,

multiplied by the constant a;

• (i) − a(j)—subtraction from the i-th row of the matrix of the row with number

j, multiplied by the constant a;

• (i) ↔ (j )—exchange of two rows.

Similar designations will also be used for operations with columns, and the

column with number j will be denoted by [j].

Example 2.18 Find the rank of the matrix

⎡

⎤

3 −1 3 2 5

5 −3 2 3 4

1 −3 −5 0 −7

7 −5 1 4 1

⎢

⎥

⎢

⎥

⎢

⎥

(2.66)

⎢

⎥ .

⎢

⎥

⎣

⎦

⎤

**Solution** Swap the ﬁrst and the third rows:

⎡

1 −3 −5 0 −7

⎢

⎥

⎢

⎥

5 −3 2 3 4

3 −1 3 2 5

7 −5 1 4 1

⎢

⎥

(2.67)

⎢

⎥ .

⎢

⎥

⎣

⎦

To the second row, add the elements of the ﬁrst row, multiplied by (−5), to the

third—by (−3) and to the fourth—by (−7). As a result we obtain

⎡

⎤

1 −3 −5 0 −7

0 12 27 3 39

0 8 18 2 26

0 16 36 4 50

⎢

⎥

⎢

⎥

⎢

⎥

(2.68)

⎢

⎥ .

⎢

⎥

⎣

⎦





64

2

Matrix Algebra

Divide the second row by 3, and the third and fourth rows by 2:

⎡

⎤

1 −3 −5 0 −7

0 4 9 1 13

0 4 9 1 13

0 8 18 2 25

⎢

⎥

⎢

⎥

⎢

⎥

(2.69)

⎢

⎥ .

⎢

⎥

⎣

⎦

Then subtract from the third row the second one, and from the fourth row the

doubled second one:

⎡

⎤

⎡

⎤

1 −3 −5 0 −7

1 −3 −5 0 −7

0 4 9 1 13

0 0 0 0 −1

0 0 0 0 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 4 9 1 13

0 0 0 0 0

0 0 0 0 −1

⎢

⎥

⎢

⎥

→(3)↔(4)

.

(2.70)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦

We have obtained the echelon form of the matrix. The number of non-zero rows

is three and therefore the rank of this matrix is three.

There is one more method to calculate the matrix rank. It is referred to as the

**bordering minor method** and consists in the following. For computing the variable

rk A, consecutively compute the minors, passing from the lower order minors to the

higher order minors. If the r-th order minor is already found

⎡

⎤

a11 . . . a1r

⎢

⎥

M = . . . . . . . . . .

⎢

⎥

,

(2.71)

⎣

⎦

ar1 . . . a

rr

that is other than zero, then it is enough just to compute the minors of the (r + 1)-th

order, bordering the minor M:

⎡

⎤

a11 . . . a1r a1t2

⎢

⎥

⎢

⎥

. . . . . . . . . . . . . . . .

⎢

⎥

for all t , t > r.

(2.72)

⎢

⎥

1

2

⎢

⎥

ar1 . . . a

rr

a

⎣

rt ⎦

2

at11 . . . at1r

a

t1t2

If they all appeared to be equal to zero, we obtain rk A = r.

The bordering minor method is especially convenient for the problems where

functional matrices are present, or the matrices whose elements depend on the

parameters (see, for example, Problem [**2.60**](#br89)).





Problems

65

**Review Questions**

\1. What is a determinant of the second order? of the third order?

\2. Formulate the rule of triangle for computing a determinant of the third order.

\3. Deﬁne the concept of inversion.

\4. Write a formula for the determinant of the n-th order.

\5. How are the additional minor Mij of the element aij and its cofactor Aij

interconnected?

\6. Formulate Laplace theorem.

\7. Enumerate the general properties of determinants.

\8. What matrix transformations are elementary?

\9. What is an inverse matrix?

\10. What matrix is called degenerate?

\11. What is the method of mathematical induction used for?

\12. How are the functions of matrices computed?

\13. Deﬁne exponential and logarithm of a matrix.

\14. Which rows are linear dependent?

\15. Formulate the theorem of a basic minor.

\16. What is the elementary transformations method based on?

\17. Enumerate the methods of ﬁnding the matrix rank.

**Problems**

**2.1**. Expand the deﬁnition ([2.5](#br60)) for the case n = 3.

**2.2**. Find the number of inversions in the permutation (5, 1, 4, 3, 6, 8, 7, 2).

**2.3**. How many inversions are there in the permutation (n, n − 1, . . . , 2, 1)?

**2.4**. Find the number of inversions in each permutation of a collection of 2n

numbers:

(1) (1, 3, 5, 7, . . ., 2n − 1, 2, 4, 6, . . ., 2n);

(2) (2, 4, 6, . . ., 2n, 1, 3, 5, 7, . . . , 2n − 1).

**2.5**. With what sign does the summand an1an−1,2 . . . a2,n−1a1n appear in the

expression for the determinant [(](#br60)[2.5](#br60))?

**2.6**. Compute the third order determinants:















3 −2 1

1 2 0

2 0 5












(1) −2 1

3

` `; 2 

( ) 0 1 3

` `; 3 

( ) 1 3 16

` `;









` `2 0 −2

5 0 −1

0 −1 10





66

2 Matrix Algebra















2 −1 3

2 1 0

2 0 0












(4) −2 3 2

` `; 5 

( ) 1 0 3

` `; 6 

( ) 3 3 0 .










` `0 2 5

0 5 −1

4 4 4

**2.7**. Compute the determinants of the fourth order:












−3 0 0 0

2 2 0 0

1 3 −1 0

2 −1 3 4

0 −1 5 −3

0 0 5 −3

2 −1 1 0

0 1 2 −1

3 −1 2 3
























(a)

; (b)

; (c)

.
























−1 5 3 5

0 0 0 2 

3 1 6 1 

**2.8**. Solve the following equation relative to the variable x:




1 1 1

1 x 1 1

1 1 x 1

x







= 0.








1 1 1

x

**2.9**. Compute the determinant




1 1 1 . . . 1

1

1

1





1 2 1 . . . 1

1 1 3 . . . 1









` `,


. . . . . . . . . . . . . .




1 1 1

1

. . . p




1 1 1

1

\+ 1

. . .

p

where p is a natural number.

∗**2.10.** Compute the determinant of the matrix Q of size n × n, whose elements are

equal to

(a) qij = δ

(b) qij = δ

\+ δ

− δ

,

i,j+1

i,j+1

i+1,j

i+1,j

for all 1  i, j  n. Here δk1,k2 is the Kronecker symbol (see page [4](#br19)).





Problems

67

**2.11**. **Fibonacci[**2](#br81)[ ](#br81)sequence**

Fn = 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, . . . for n = 1, 2, . . .

is determined by the recur[ren](#br421)[ce](#br422)[ ](#br422)[r](#br422)elation: F

= Fn + Fn+1 with the initial

n+2

conditions F = F = 1 [[28](#br421)[,](#br421)[ ](#br421)[70](#br422)[\].](#br422)

1

2

Prove that the (n + 1)-the term of the Fibonacci sequence is equal to the

determinant of the n-th order

⎡

⎤

1

1 0 0 . . . 0

0

0

⎢

⎥

⎢

⎥

−1 1 1 0 . . . 0

⎢

⎥

⎢

⎥

⎢ 0 −1 1 1

0

0 ⎥

. . .

⎢

⎥

⎢

⎥

F +1 = ⎢ . . . . . . . . . . . . . . . . . . . . ⎥ .

(2.73)

n

⎢

⎥

⎢

⎥

0

0

0

0 0 0 . . . 1

0

⎢

⎥

⎢

⎥

⎢

⎥

0 0 0 . . . 1

1

⎣

⎦

0 0 0 . . . −1 1

∗**2.12.** The **Vandermonde[**3](#br81)[ ](#br81)determinant** is the determinant of size n×n, composed

of the real numbers a , a , . . . , a :

1

2

n




` `1

1

1

. . .

1





` `a1

a2

a3 . . . an



Vn =

2

1

2

2

2

3

2

n

.

(2.74)

a

a

a

. . .

a



` `. . . . . . . . . . . . . . . . . . . . . . . . 




−1 n−1 n−1 −1

. . . a

n

` `n

n

a

a

a

1

2

3

(1) Verify that for n = 2 this determinant is equal to V = a − a .

2

2

1

(2) By the mathematical induction method, prove that the Vandermonde

determinant Vn is equal to the product of all the possible differences

a − a for 1  i < j  n:

j

i

"

Vn =

(a − a ).

(2.75)

j

i

i<j

2Under the name Fibonacci is known Middle Age mathematician Leonardo Pisano (about 1170—

about 1250).

3Alexandre-Théophile Vandermonde (1735–1796), French mathematician and musician.





68

2 Matrix Algebra

**2.13**. Let A be a matrix of size n × n, m is an arbitrary natural number. Is it true

that the equality det(mA) = mn det A is fulﬁlled?

**2.14**. At the examination in linear algebra, the student says that the determinant

of the sum of two matrices is always equal to the sum of the determinants of

these matrices: det(A + B) = det A + det B. Is the student right?

**2.15**. Is the determinant





1

1

1

1

10000




10000

1

1

1

1

1

1

1






(2.76)

1

1

1

1

10000

1

1

1

10000





1

1






10000

a positive number, a negative number or zero?

**2.16**. Is the determinant





1

5

4

3

10000

3

4

5





1

5

4

3

2

3

10000






(2.77)

1

10000

4

10000

3

2

1





1

5





10000

a positive number, a negative number or zero?

**2.17**. Using Python, compute the determinants in Problems [**2.15**](#br82)[** ](#br82)and [**2.16**](#br82)[** ](#br82)and

verify the correctness of the solutions of these problems.

**2.18**. Find the number of minors of the k-th order in a matrix consisting of m rows

and n columns.

**2.19**. How many minors of the k-th order in a matrix of size n × n do not contain

diagonal elements of the original matrix?

∗**2.20.** What greatest value can take the determinant of a matrix of size 3 × 3,

consisting of the elements +1 and −1?

∗**2.21.** What greatest value can take the determinant of a matrix of size 3 × 3,

consisting of the elements 0 and 1?

**2.22**. Will the determinant of the matrix change if its columns are permuted in the

reverse order?

**2.23**. **Computing the determinant of the matrix using Python**

In the text ﬁle input.txt are successively written in rows the elements

of the integer square matrix A. Using the recursion, compute the determinant

det A. Enter the result into the text ﬁle output.txt.





Problems

69

**2.24**. Evaluate the number of multiplications executed by the recursive algorithm

for computing the determinant of the matrix of size n × n (see previous

Problem).

∗**2.25.** Prove that the exact number of multiplications executed by the recursive

algorithm for computing the determinant of the matrix of size n × n (see

Problems [**2.23**](#br82)[** ](#br82)and [**2.24**](#br82)) is equal to

T (n) = en(n, 1) − n!,

#∞

where e is the base of natural logarithms, (n, x) =

e−t tn−1dt—

$

x

**incomplete gamma function** for the natural n ∈ N the following equality

%

n−1 xk

is true (n, x) = (n − 1)! e−x

.

k!

k=0

∗**2.26.** Obtain the asymptotic estimate of the mean value of the number of

inversions A(N) in the array consisting of N elements, for N → ∞.

∗**2.27.** Prove the validity of the identity

det(I + εB) = 1 + ε tr B + O(ε2) for ε → 0,

(2.78)

where B is some square matrix, I is an identity matrix of the same size.

∗**2.28.** Obtain the asymptotic estimate of the variable


I

det

for ε → 0,

(2.79)

(I + εB)p

if B is an arbitrary square matrix, I is the identity matrix of the same size,

p ∈ N.

∗**2.29.** Assume that M = G + εH, where ε is a real number, G is an invertible ma-

trix. Relying upon the equality det A = exp(tr ln A) (see the Theorem [2.5](#br73)

on page [59](#br73)), prove that

det M

1

= det G 1 + εtr (G−1H) + ε (tr (G−1H) − tr (G−1H) ) + O(ε )

2

2

2

3

2

(2.80)

for ε → 0.

**2.30**. Assume that the real parameters a, b, c and d are selected, such that the

⎡

⎤

a b

inequality ad −bc = 0 is valid. Compute the matrix inverse of A = ⎣ ⎦.

c d





70

2

Matrix Algebra

**2.31**. Find the inverse matrices of the following matrices:

⎡

⎤

⎡

⎤

1 2

3 4

(1)

⎣

⎦ ;

( )

2

⎣

⎦ ;

3 4

5 7

⎡

⎤

⎡

⎤

⎡

⎤

3 −4 5

2 7 3

1 5 3

1 2

2

⎢

⎥

⎢

⎥

⎢

⎥

(3) 2 −3 1

⎢

⎥ ;

( ) 3 9 4

4

⎢

⎥ ;

5

( ) 2 1 −2

⎢

⎥

.

⎣

⎦

⎣

⎦

⎣

⎦

3 −5 −1

2 −2 1

**2.32**. Find the inverse matrices of the following matrices:

⎡

⎤

⎡

⎤

1 1 1 1

0 2 2 2

0 0 3 3

0 0 0 4

⎡

⎣

⎤

1 1 1

⎢

⎥

⎢

⎥

1 1

⎢

⎥

⎢

⎥

(1)

⎦ ;

( ) 0 2 2

2

⎢

⎥ ;

( ) ⎢

3

⎥ .

⎣

⎦

⎢

⎥

0 2

⎣

⎦

0 0 3

**2.33**. Calculate the commutators [A, A−1] and [A, A−1], if A is an arbitrary

nonsingular matrix.

**2.34**. For what values of the real parameter λ the matrix does not have the inverse

one?

⎡

⎤

−1 λ λ

⎢

⎥

(1) ⎢

0⎥ ;

λ λ

⎣

⎦

6 4 λ

⎡

⎤

3

λ

λ

⎢

⎥

(2) ⎢

−1⎥ .

−1 −1 λ

λ

λ

⎣

⎦

**2.35**. Compute the matrix inverse of A:

⎡

⎤

1 α 0 0

0 1 β 0

0 0 1 γ

0 0 0 1

⎢

⎥

⎢

⎥

⎢

⎥

A = ⎢

⎥ ,

⎢

⎥

⎣

⎦

where α, β, γ ∈ R. Does the matrix A−1 exist for all possible values of the

parameters?





Problems

71

∗**2.36.** Compute the matrix inverse of Gn of size n × n, where n  2:

⎤

0 0 0 . . . 0 1

⎢

⎥

⎢

⎥

0 0 0 . . . 1 0

⎢

⎥

⎥

⎥

.

(2.81)

⎥

⎥

. . .

0 0 ⎥

⎦

**2.37**. The elements of a **Hilbert[**4](#br85)[ ](#br85)matrix** H = (h ) are set by the rule h

\=

ij

ij

1

, where i, j = 1, 2, . . . , n.

i + j − 1

With the help of Python, compute H−1, H · H−1 and H−1 · H for n =

6, 7, 8.

∗**2.38.** Find the inverse of the following matrix:

⎡

⎤

1 λ λ2 λ3 . . . λn

⎢

⎥

⎢

⎥

0 1 λ λ2 . . . λn−1

⎢

⎥

⎢

⎥

⎢

n−2 ⎥

0 0 1 λ . . . λ

,

⎢

⎥

⎢

⎥

⎢. . . . . . . . . . . . . . . . . . .⎥

⎣

⎦

0 0 0 0 . . .

1

where λ is some real number.

**2.39**. With the help of the mathematical induction method, prove the **matrix**

**product inversion formula**

−1

−1 −1

−1 −1

. . . A A .

2 1

(A1A2 . . . A −1A ) = A

A

(2.82)

n

n

n

−1

n

**2.40**. Solve the matrix equations:

⎡

⎤

⎡

⎤

2 1

−6 4

(1) ⎣ ⎦ · X = ⎣

⎦ ;

0 2

2 1

⎡

⎤

⎡

⎤

−1 1 1

−2 1 1

⎢

⎥

⎢

⎥

(2) ⎢ 0 2 2⎥ · X = ⎢−1 0 2⎥ ;

⎣

⎦

⎣

⎦

0 2 3

−1 −2 0

4David Hilbert (1862–1943), German mathematician.





72

2 Matrix Algebra

⎡

⎤

⎡

⎤

1 10 −3

0 −1 2

⎢

⎥

⎢

⎥

(3) X · ⎢−3 6 2 ⎥ = ⎢−1 −2 −2⎥ ;

⎣

⎦

⎣

⎦

2

6 −3

0

1 10

⎡

⎤

⎡

⎤

⎡

1 −1

0 1

⎤

2 3

1 7

(4) ⎣

⎦ · X · ⎣ ⎦ = ⎣

⎦ .

−3 2

5 4

**2.41**. Assuming that a is an arbitrary real number, raise the matrix of power:

⎡

⎤

256

1 0 0

0 1 0

0 a 1

⎢

⎥

⎢

⎥

(2.83)

.

⎣

⎦

∗**2.42.** Raise the matrix of power:

⎡

⎤

512

1 0 0

g 1 0

h 0 1

⎢

⎥

⎢

⎥

(2.84)

,

⎣

⎦

where constants g, h ∈ R.

**2.43**. Using the mathematical induction method, prove that the n-th power of the

⎡

⎤

0 1

matrix F = ⎣ ⎦ has the form

1 1

⎡

⎤

Fn−1

F

F

n = ⎣

n ⎦

(2.85)

Fn F +1

n

for all natural values n > 1, where Fn are the Fibonacci numbers (see

deﬁnition in Problem [**2.11**](#br81)[** ](#br81)on page [67](#br81)).

⎡

⎤

1 α γ

0 1 β

0 0 1

⎢

⎥

**2.44**. Compute the n-th power of the upper triangular matrix A = ⎢

⎥ ,

⎣

⎦

where α, β, γ ∈ R.





Problems

73

**2.45**. Compute the q-th power of the functional matrix

⎡

⎤

⎦

cos ϕ sin ϕ

U(ϕ) =

⎣

− sin ϕ cos ϕ

for all integer values of q ∈ Z.

**2.46**. It is known about the matrices A and B that their commutator is the identity

matrix: [A, B] = I. Compute [A, Bq] for all integer values of the parameter

q ∈ Z.

**2.47**. Compute the value of the function f (x) = x2 − 3x + 2, if as the argument

is taken the matrix A, where

⎡

⎤

1 0

(1) A = ⎣ ⎦;

0 1

⎡

⎤

1 −2

−3 1

(2) A = ⎣

⎦.

**2.48**. Compute the value of the function g(x) = x3 + x − 3, if as the argument is

taken the matrix A, where

⎡

⎤

1 0 0

⎢

⎥

(1) A = ⎢1 1 0⎥;

⎣

⎡

⎦

1 1 1

⎤

−2 1 0

⎢

⎥

(2) A = ⎢ 3 −1 1⎥.

⎣

⎦

2

1 0

**2.49**. Compute the value of the fractionally rational function g(A), if g(x) =

3 + 2 − 3 − 5

x

x

x

and

x

3 − 5 − 2

x

⎡

⎤

2 0 0

⎢

⎥

(1) A = ⎢0 −4 0⎥;

⎣

⎡

⎦

0 0 1

⎤

1 1 0

⎢

⎥

(2) A = ⎢0 1 0⎥.

⎣

⎦

0 1 1





74

2 Matrix Algebra

**2.50**. Show that the equality

⎡

⎤

⎡

⎤

⎦

0 −1

1 0

cos 1 − sin 1

sin 1 cos 1

exp⎣

⎦ = ⎣

is valid.

**2.51**. Find eA for

⎡

⎤

1 0 0

⎢

⎥

(1) A = ⎢0 1 0⎥;

⎣

⎡

⎦

⎤

0 0 0

0 1 0

⎢

⎥

(2) A = ⎢0 0 1⎥.

⎣

⎦

⎤

0 0 0

∗**2.52.** Find eA for

⎡

1 0 1

⎢

⎥

(1) A = ⎢0 1 0⎥;

⎣

⎡

⎦

⎤

0 0 1

1 0 1

⎢

⎥

(2) A = ⎢1 1 1⎥.

⎣

⎦

0 0 1

**2.53**. For the matrices speciﬁed in the previous problem, compute ln A.

∗**2.54.** Prove that for the commuting matrices the exponential of the sum is equal

to the product of the exponentials of each of the summands:

exp(A + B) = exp(A) exp(B).

**2.55**. Prove that exp(tA) = I + tA + O(t2) for t → 0.

**2.56**. Consider all possible matrices of size 3 × 3 that contain no zero column.

Enumerate pairwise various echelon forms of such matrices.

**2.57**. Which elementary operations with the elements of the echelon matrix

preserve its echelon form?

**2.58**. Find the ranks of the matrices:





Problems

75

⎡

⎤

⎡

⎢

⎤

⎥

2 −4 3 1 0

1 −2 1 −4 2

0 1 −1 3 1

4 −7 4 −4 5

1

2 −4 3 −2

⎢

⎥

⎢

⎥

⎢

⎥

(1) A = ⎢−1 3 −6 −2 4 ⎥ ; (2) A =

;

⎢

⎥

⎣

⎦

⎢

⎥

⎣

⎦

2 −1 2

5

6

⎡

⎤

⎡

⎢

⎤

0

2

−4

1 2

1

3

⎢

⎥

⎢

⎥

⎥

−1 −4 −5

⎢

⎥

⎢

⎥

4 −1 −5 −6

1 −3 −4 −7

2 1 −1 0

⎢

⎥

⎢

⎥

(3) A =

; (4) A = ⎢ 3

1

7 ⎥ ;

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎢ 0 5 −10⎥

⎣

⎦

2

3

0

⎡

⎤

⎡

⎤

3 5 7

4 3 2 2

⎢

⎥

⎢

⎥

(5) A = ⎢1 2 3⎥ ; (6) A = ⎢0 2 1 1⎥ ;

⎣

⎦

⎣

⎦

1 3 5

0 0 3 3

⎡

⎤

⎡

⎢

⎤

⎥

1 3 5 −1

2 −1 −3 4

5 1 −1 7

1 −1 2 4 3

⎢

⎥

⎢

⎥

⎢

⎥

(7) A = ⎢−2 1 5 2 6⎥ ; (8) A =

.

⎢

⎥

⎣

⎦

⎢

⎥

⎣

⎦

2 −1 4 7 2

7 7

9

1

**2.59**. With the help of the bordering minor method, ﬁnd the maximum value that

the rank of the matrix  can take

⎡

⎤

β − γ

0

γ −β

⎢

⎥

` `= γ − α −γ

⎢

0

⎥

,

α

⎣

⎦

α − β β −α 0

if α, β and γ are real constants.

∗**2.60.** Find the ranks of the following matrices for all possible values of the real

parameter λ:

⎡

⎤

1 λ 0

⎢

⎥

(a) ⎢1 1 0⎥ ;

⎣

⎦

0 0 1





76

2 Matrix Algebra

⎡

⎤

1 − λ

0

2 −

0

0

0

⎢

⎥

(b) ⎢

⎥ ;

0

λ

⎣

⎦

0

3 − λ

⎡

⎤

1

2

−3

⎢

⎥

(c) ⎢−1 2 −

10 ⎥ ;

λ

λ

⎣

⎡

⎦

⎤

−1

−λ

0

1

3 − λ

1

⎢

⎥

(d) ⎢ 0 1 −

⎥ ;

1

⎣

⎦

0

1

0

2 − λ

⎡

⎤

−6 −5

⎢

⎥

(e) ⎢−1 2 −

⎥ ;

λ

5

⎣

⎡

⎦

−1

6

1 − λ

⎤

1 − λ

2

0

0

⎢

⎥

⎢

⎥

1

2 − λ

0

0

0

⎢

⎥

(f)

(g)

(h)

;

;

⎢

⎥

⎢

⎥

0

3 − λ

0

0

4 − λ

0

⎣

⎦

0

0

⎡

⎤

1 − λ

2

1 + λ

0

0

0

⎢

⎥

⎢

⎥

1

0

0

0

⎢

⎥

⎢

⎥

⎢

⎥

2 − λ

0

0

⎣

⎦

0

2 + λ

⎡

⎤

1 + λ 2

0

0

4

0

⎢

⎥

⎢

⎥

1

1

⎢

⎥

;

⎢

⎥

⎢

⎥

0

0 2 + λ −1

0

⎣

⎡

⎦

1

2

1

⎤

−λ

⎢

1

1

1

1 . . .

1 . . .

1

1

1

1

⎢

⎥

⎢

⎥

0 1 − λ

0

1

1

⎥

⎢

⎥

⎢

⎥

0

2 − λ 1 . . .

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎢

⎥

(i)

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢ 0

0

0

0

0

0

− 1 −

1

⎥

. . . (n

)

λ

⎣

⎦

0

0 . . .

0

n − λ





Answers and Solutions

77

**Answers and Solutions**

[**2.1**](#br79)[** ](#br79)Solution.

For n = 3 we have 3! = 1 · 2 · 3 = 6 permutations:

k1 = 1, k2 = 2, k3 = 3; k1 = 1, k2 = 3, k3 = 2; k1 = 2, k2 = 1, k3 = 3;

k1 = 2, k2 = 3, k3 = 1; k1 = 3, k2 = 1, k3 = 2; k1 = 3, k2 = 2, k3 = 1.

Therefore, the sum in det A will consist of 6 terms, half of which is taken with a

positive sign, and another half—with a negative sign:

det A =

(−1)σ a1k1 a2k2a3k3

perm

0

1

1

= (−1) a a a + (−1) a a a + (−1) a a a

\+ (−1) a a a + (−1) a a a + (−1) a a a

11 22 33

2

11 23 32

2

12 21 33

3

12 23 31

13 21 32

13 22 31

= a a a + a a a + a a a

11 22 33

12 23 31

13 21 32

− a a a − a a a − a a a .

13 22 31

12 21 33

11 23 32

The obtained formula, of course, conforms with the deﬁnition ([2.3](#br58)).

[**2.2**](#br79)[** ](#br79)Answer: the number of inversions is equal to 10.

[**2.3**](#br79)[** ](#br79)Solution.

The ﬁrst element of the permutation, equal to n, forms n − 1 inversions paired

with each of the elements n−1, n−2, ..., 1. The second element of the permutation

n − 1 forms with the remaining elements n − 2 inversions. As is easy to see,

the permutation element, equal to k, where 1  k  n, forms k − 1 inversions.

Therefore, the total number of inversions in the permutation (n, n − 1, . . . , 2, 1) is

n

equal to the sum

k = n(n − 1)/2.

k=1

[**2.4**](#br79)[** ](#br79)Answer:

n(n − 1)

(1)

(2)

;

.

2

n(n + 1)

2

[**2.5**](#br79)[** ](#br79)Solution.

The summand a a

n1 n−1,2

. . . a

2,n−1 1n

a

in the formula ([2.5](#br60)) is assigned the sign

(−1)

σ = −1 n(n−1)/2, since the number of inversions in the permutation

(

)

(n, n

−

1, . . . , 2, 1) is equal to σ = n(n − 1)/2 (see Problem [**2.3**](#br79)).





78

2 Matrix Algebra

Note. With the help of the function “ﬂoor” x —the greatest integer, which is

less than or equal to the argument x, i.e. x = max(n ∈ Z, n  x), the answer

can be written in a more compact form: (−1)σ = (−1)n/2 .

[**2.6**](#br79)[** ](#br79)Solution.

(1) Calculate the determinant, using the rule of triangle for calculation by the

formula ([2.3](#br58)).





3 −2 1





` `= 3 · 1 · −2 + −2 · 3 · 2 + 1 · −2 · 0

−2 1

3

(

)

(

)

(

)



` `2 0 −2

− 1 · 1 · 2 − (−2) · (−2) · (−2) − 3 · 3 · 0 = −12.

(2) Expand the determinant in the ﬁrst row:











1 2 0

0 1 3










1 3 

0 3 

0 1

` `= 1 

` `− 2 

` `+ 0 










0 −1

5 −1

5 0

5 0 −1

= 1 · (1 · (−1) − 0 · 3) − 2 · (0 · (−1) − 3 · 5) + 0 · (0 · 0 − 5 · 1)

= −1 + 30 = 29.

(3) Expand the determinant in the ﬁrst row:





2 0

5





` `= 2 · 3 · 10 − −1 · 16 − 0 · 1 · 10 − 0 · 16

\+ 5 · ((−1) · 1 − 0 · 3)

= 92 − 5 = 87;

1 3 16

(

(

)

)

(

)



0 −1 10

(4) Expand the determinant, for example, in the third row:





2 −1 3





` `= 0 · 3 · 3 − −1 · 2 − 2 · 2 · 2 − −2 · 3

−2 3 2

(

(

)

)

(

(

)

)



` `0 2 5

\+ 5 · (2 · 3 − (−2) · (−1)) = −20 + 20 = 0.





Answers and Solutions

79

(5) Expand the determinant in the ﬁrst row:





2 1 0

1 0 3





` `= 2 · 0 · −1 − 5 · 3 − 1 · 1 · −1 − 0 · 3 + 0 · 1 · 5 − 0 · 0

= −30 + 1 = −29.

(

(

)

)

(

(

)

)

(

)



0 5 −1

(6) The determinant of the lower triangular matrix is calculated as the product of

its diagonal elements:





2 0 0





` `= 2 · 3 · 4 = 24

3 3 0

.



4 4 4

[**2.7**](#br80)[** ](#br80)Solution.

(a) Expand the determinant in the ﬁrst row:




−3 0 0 0

2 2 0 0

1 3 −1 0



















2 0 0

2

0 0

2 2 0
















= −3 · 3 −1 0 − 0 ·  1 −1 0 + 0 ·  1 3 0















5 3 5

−1 3 5

−1 5 5


−1 5 3 5





2 2 0




− 0 ·  1 3 −1 = −3 · (−10 + 0 + 0 − 0 − 0 − 0)



−1 5 3 

− 0 + 0 − 0 = 30.

Note that the original matrix is the lower triangular one, hence its determi-

nant can be calculated by a simpler method as the product of diagonal elements:

` `= (−3) · 2 · (−1) · 5 = 30.

(b) Expand the determinant in the ﬁrst column:




2 −1 3 4

0 −1 5 −3

0 0 5 −3



















−1 5 −3

−1 3 4

−1 3 4

















= 2 ·  0 5 −3 − 0 ·  0 5 −3 + 0 · −1 5 −3














` `0 0 2 

` `0 0 2 

` `0 0 2 


0 0 0 2 





80

2 Matrix Algebra





−1 3 4




− 0 · −1 5 −3 = 2 · (−10 + 0 + 0 − 0 − 0 − 0) − 0



` `0 5 −3

\+ 0 − 0 = −20.

The result can be obtained faster if we note that the matrix is the upper

triangular one. Then  = 2 · (−1) · 5 · 2 = −20.

(c) Expand the determinant in the ﬁrst row:




2 −1 1 0

0 1 2 −1

3 −1 2 3



















1 2 −1

0 2 −1

0 1 −1
















= 2 · −1 2 3  − (−1) · 3 2 3  + 1 · 3 −1 3 















` `1 6 1 

3 6 1 

3 1 1 


3 1 6 1 




0 1 2




− 0 · 3 −1 2 = 2 · (2 + 6 + 6 + 2 − 18 + 2)

− (−1) · (0 + 18 − 18 + 6 − 0 − 6)

\+ 1 · (0 + 9 − 3 − 3 − 0 − 3) − 0 = 0.




3 1 6

[**2.8**](#br80)[** ](#br80)Solution.

Denote the determinant by  and expand it in the ﬁrst row. We will expand the

obtained third order determinants in the ﬁrst row or in the row consisting of ones, if

any:

















1 1

1 1 1

1 x 1

1 x 1

1 1 x

x















` `= x 1 x 1

` `− 

1 x 1

` `+ 

1 1 1

` `− 
















1 1

1 1

1 1

1 1 1

x

x

x




2

2

= x x(x − 1) − (x − 1) + (1 − x) − (x − 1) − (x − 1) + (1 − x)




2

2

\+ − (x − 1) + (x − 1) − (1 − x) − (x − 1) − (x − 1) + (1 − x)

3

2

2

2

= x(x − 3x + 2) − 3(x − 2x + 1) = x(x − 1)(x + x − 2) − 3(x − 1)

3

2

3

= (x − 1)(x + x − 5x + 3) = (x − 1) (x + 3).

As a result, the roots of the equation  = 0 are equal to x = 1 and x = −3.





Answers and Solutions

81

[**2.9**](#br80)[** ](#br80)Solution.

Apply to the determinant the following equivalent transformations: from each

row, starting with the second one, subtract the ﬁrst one. As a result we obtain the

determinant of the upper triangular matrix:




1 1 1 . . .

1

0

0

0

1




0 1 0 . . .

0 0 2 . . .

0 0 0 . . .

0

0

0









` `.






0 0 0

− 1 0

. . . p

. . .




0 0 0

0

p

Such a determinant is equal to the product of the diagonal elements of the matrix:

1 · 1 · 2 . . .(p − 1) · p = p!.

[**2.10**](#br80)[** ](#br80)Solution.

(a) Denote the determinant of the matrix Q by Qn and write it in an explicit form:




0 1 0 0 . . . 0 0 




1 0 1 0 . . . 0 0

0 1 0 1 . . . 0 0

. . . . . . . . . . . . . .








Q = 

` `.

n






0 0 0 0

0 1 

. . .

. . .




0 0 0 0

1 0 

Let us use the expansion in its ﬁrst row, following which expand the obtained

the determinant of order (n − 1) × (n − 1) in the ﬁrst column:






1 1 0 . . . 0 0 




0 1 . . . 0 0 


0 0 1 . . . 0 0

0 1 0 . . . 0 0

. . . . . . . . . . . . .








1 0

. . .

0 0








Qn = (−1)1+2 · 

` `= (−1)1+2(−1)

1+1 

· . . . . . . . . . . . . .









0 0

0 1 


. . .


0 0 0

0 1 

. . .

. . .




0 0

1 0 


. . .

0 0 0

1 0 





82

2 Matrix Algebra

Note that the problem reduced to computing the variable Q . For the

n−2

smallest possible values of the order of the matrix n = 1 and n = 2 we have

⎡

⎤

0 1

Q1 = det[0] = 0, Q2 = det

⎣

⎦ = −1

.

1 0

Thus, the recurrence relation is obtained:

Q = −Q

1

,

n

n−2

2

Q = 0, Q = −1.

By the mathematical induction method we can show that its solution Qn will

have the form:

(−1)n/2,

0,

if is even

n

,

Qn =

if n is odd.

(b) Using Laplace’s method, similarly to item (a) we obtain the recurrence relation:

Q = Q

1

,

n

n−2

Q = 0, Q = 1.

2

Its solution, as is easy to show with the help of the mathematical induction

method, has the form:

1

Qn = 1 + (−1) .

n

2

[**2.11**](#br81)[** ](#br81)Solution.

Denote by P (n) the predicate “F

nant ([2.73](#br81)). Let us use the mathematical induction method.

B a s i s s t e p

= D(n)”, where D(n) is the determi-

n+1

For n = 1 and n = 2 we have







1

1 0




` `1 1


F2 =

` `—true,

F3

\= 

−1 1 1

` `—true.




−1 1

` `0 −1 1

I n d u c t i v e s t e p

Assume the trueness of the statements P (k) for k = 1, 2, . . ..

Prove that this entails the trueness of P(k + 1).





Answers and Solutions

83

Indeed, expanding the determinant D(n + 1) in the ﬁrst row, we obtain

D +1 = D + D −1.

n

n

n

According to the inductive supposition D(n) = F , D(n − 1) = F .

n+1

n

Therefore, we have obtained the true equality F

= F

\+ F .

n+2

n+1

n

Thus, the mathematical induction method has proved that F

= D(n) for all

n+1

natural n.

[**2.12**](#br81)[** ](#br81)Solution.

(1) According to the deﬁnition of ([2.74](#br81)) for n = 2 we have




` `1 1 

Vn =

` `=

a2 a1.

−


a a 

1

2

(2) Let us introduce for consideration the predicate “V =

(a − a )” and

n

j

i

i,j∈[1,n]

i<j

denote it by P (n).

B a s i s s t e p

The case of the least n = 2 is proved in item (1) of this problem.

I n d u c t i v e s t e p

Let for some natural k  2 the equality be fulﬁlled Vk =

(a − a ).

j

i

i,j∈[1,k]

i<j

Prove that Vk+1

\=

(a − a ).

j

i

i,j∈[1,k+1]

i<j

Transform V

as follows: from the (k + 1)-th row subtract the k-th one,

k+1

multiplied by a , then from the k-th one subtract the (k − 1)-th one, also multiplied

1

by a and so until the second row inclusive:

1




1

1

1

. . .

. . .

1





0

a − a

a − a

a − a a . . . a

a

− a1

2

1

3

1

+1

k


V +1 = 0 a − a a

2

2

2

2

k

− a a

.

k

1

2

3

1

3

+1

1

k+1 


` `. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 




k

2

−1

k −

k−1

. . . ak

−

k−1

0 k −

a

a1a

a

a1a

a1a

2

3

3

k+1

k+1

The ﬁrst column of the obtained determinant is formed by zeroes, except the

element in the upper left corner, equal to one. Using this fact, it is easy to perform

the expansion in the ﬁrst column. After taking the common multipliers outside the





84

2 Matrix Algebra

sign of determinant, we have




` `1

1

. . . 1 




` `a2 a3 . . . a +1

k


V +1 = (a2 − a1)(a3 − a1) . . . (a +1 − a1)

2

2

2

3

2

.

a

a

. . . a

+1

k

k

k


` `. . . . . . . . . . . . . . . . . 




−1 k−1

. . . a

k−1

` `k

a

a

2

3

k+1

As a result we have obtained the determinant V , which, according to the

k

inductive supposition, is equal to the product of all the possible differences a − a

j

i

for 1  i < j  k.

Therefore, the mathematical induction method has proved the formula of ([2.75](#br81)).

Note. The Vandermonde matrix, i.e. a matrix of the form




` `1

1

. . . 1 




` `a1 a2 . . . a

n



2

1

2

2

2 

` `a

a

. . . a

n


` `. . . . . . . . . . . . . . . . . 




−1 n−1

−1

. . . a

n

` `n

n

a

a

1

2

is widely met in the theory of approximation of functions by polynomials [[11](#br420)[,](#br420)[ ](#br420)[58](#br422)[\].](#br422)

[**2.13**](#br81)[** ](#br81)Solution.

In case of multiplication of any row by a real number, the determinant of this

matrix is multiplied by this number. Therefore, as all the elements of the matrix A

are multiplied by m, the determinant is multiplied by the value

m × m × · · · × m .



!

n times

Thus, for all m ∈ N the equality det(mA) = mn det A is fulﬁlled.

[**2.14**](#br82)[** ](#br82)Solution.

The student is wrong. The determinant of the sum of two matrices is not always

equal to the sum of the determinants of these matrices, which is conﬁrmed by the

following counterexample.

Consider an identity matrix of size n × n. Then the inequality is valid:

det(I + I) = det I + det I,

since det(I + I) = det(2I) = 2n (see Problem [**2.13**](#br81)). At the same time, det I +

det I = 1 + 1 = 2 = det(I + I).





Answers and Solutions

85

[**2.15**](#br82)[** ](#br82)Solution.

The expansion of the determinant by the formula [(](#br60)[2.5](#br60)) contains 5! = 120

summands. One of these summands of the form a a a a a includes all the

15 21 34 42 53

ﬁve multipliers of value 10000 and is equal to (−1)σ 100005 = (−1)σ 1020. Here

σ is the number of inversions in the permutation (5, 1, 4, 2, 3). As is easy to see,

σ = 6.

The remaining 5! − 1 = 119 summands include no more than three multipliers

10000 and, therefore, do not exceed 100003 × 1 × 1 = 1012 in absolute magnitude.

Hence it may be concluded that the considered determinant is no less than the

difference 1020 − 119 · 1012 > 0.

As a result, the determinant is positive.

[**2.16**](#br82)[** ](#br82)Solution.

Relying of the reasoning provided in the solution of Problem [**2.15**](#br82), we obtain: the

determinant in this case does not exceed the value

(−1020 + 119 · 4 · 5 · 1012) < 0.

Therefore, this determinant is a negative number.

[**2.17**](#br82)[** ](#br82)Answer:

Computing of determinants with the help of Python provides the following

results:




1

104

1

1

1

1

1

1

1 104






1

1

1





1 104

` `= 99999990001999850004

,




` `1 104

1

1

1

1 




` `1 1 104

1 




` `1 10

4

3

2

4

5





5

4

1

5

3 104





1 104

` `= −99999909053183731167

3

.




` `3 4 104

1

5

2 




104

3

4

1 

These results, of course, conform with the solution of Problems [**2.15**](#br82)[** ](#br82)and [**2.16**](#br82).

[**2.18**](#br82)[** ](#br82)Solution.

Recall that in combinatorics the number o[f](#br420)[ ](#br420)[c](#br420)[ombinations](#br422)[ ](#br422)of n various elements

of k without iterations is denoted as C(n, k) [[1](#br420)[,](#br420)[ ](#br420)[60](#br422)[\].](#br422)





86

2 Matrix Algebra

In order to form the minor of the k-th order, one should select k rows and k

columns from the matrix. The rows can be selected by C(m, k) methods, while the

columns—by C(n, k) method. Applying the combinatory rule of product, we obtain,

that all in all we can have C(m, k)C(n, k) minors of the k-th order.

[**2.19**](#br82)[** ](#br82)Answer:

The rows for formation of the minor may be selected using the number of

combinations, by C(n, k) methods. Then the columns should be selected so that

their numbers should not coincide with the numbers of the selected rows. This can

be done in C(n − k, k) ways. In all, according to the combinatory rule of product,

we obtain the answer: C(n, k)C(n − k, k) minors.

[**2.20**](#br82)[** ](#br82)Solution.

Consider the matrix A of size 3 × 3

⎡

⎤

a11 a12 a13

⎢

⎥

A =

⎢

⎥

⎣ 21

a

a22

a

23⎦

a31 a32 a33

and write its determinant in the form

det A = a a a + a a a + a a a

11 22 33

12 23 31

13 21 32

− a a a − a a a − a a a

11 23 32

12 21 33

13 22 31

= α + β + γ

\+ δ + ε + ζ,

where designations α = a a a , β = a a a , ..., ζ = −a a a are

11 22 33

12 23 31

13 22 31

introduced. Each of the variables α, β, . . . , ζ takes the values from the set {−1, 1}.

All the six summands of the determinant cannot have the same sign. Indeed, the

product αβγ can be presented in the form of the product of nine elements of the

matrix A:

3

"

αβγ =

a .

ij

i,j=1

At the same time, there exists the equality δεζ = (−1)3

3

aij = −αβγ .

i,j=1

Therefore, among α, β, . . . , ζ there exist negative summands, and det A < 6.

If ﬁve terms of the determinant have one sign, and the sixth term has a different

sign, then det A as an even number. Then, det A < 5.





Answers and Solutions

87

As is easy to ﬁnd by direct calculation, the matrix

⎡

⎤

−1

1

1

⎢

⎥

⎢

⎥

1 −1

1

⎣

⎦

1

1 −1

has det A = 4.

Finally we obtain: the greatest value of the determinant of the matrix of size 3×3,

consisting of the elements +1 and −1, is equal to 4.

[**2.21**](#br82)[** ](#br82)Answer: 2.

[**2.22**](#br82)[** ](#br82)Answer: the determinant will be multiplied by (−1)n/2 .

[**2.23**](#br82)[** ](#br82)Solution.

\# The number of multiplications

count = 0

def get\_determ(A):

global count

size = len(A)

if size == 1:

return A[0][0]

elif size == 2:

count += 2

return A[0][0] \* A[1][1] - A[0][1] \* A[1][0]

else:

det = 0

\# Expansion over the first row

for col in range(size):

minor = [row[:col] + row[col + 1:] for row in (A[1:])]

det\_sign = 1 if col % 2 == 0 else -1

det += det\_sign \* A[0][col] \* get\_determ(minor)

count += 1

return det

mas = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

print("det =", get\_determ(mas))

print("count =", count)

[**2.24**](#br82)[** ](#br82)Solution.

For the matrix of size n×n, n recursive calls are performed and n multiplications

are executed of the form a ×A , j = 1, . . . , n. The exit from the recursion will be

ij

ij





88

2 Matrix Algebra

at n = 1; no multiplications are executed in this case. Due to this, the total number

of multiplications satisﬁes the recurrence relation:

T (n) = nT (n − 1) + n, n > 1,

T (1) = 0.

Solve the obtained relation by the method of substitution, i.e. successively

expressing T (n − 1) by T (n − 2), then T (n − 2) by T (n − 3), and so on:

T (n) = nT (n − 1) + n

= n[(n − 1)T (n − 2) + n − 1] + n

= n(n − 1)T (n − 2) + n(n − 1) + n

= n(n − 1)[(n − 2)T (n − 3) + n − 2] + n(n − 1) + n

= n(n − 1)(n − 2)T (n − 3) + n(n − 1)(n − 2) + n(n − 1) + n.

Similarly continuing this process until T (1) = 0, we obtain

T (n) = n(n − 1)(n − 2) . . .2 · T (1)

\+ n(n − 1)(n − 2) . . .2 + n(n − 1)(n − 2) . . .3 + · · · + n(n − 1) + n

n!

n!

n!

= 0 + n! +

\+ · · · +

\+

2!

(n − 2)! (n − 1)!

&

'

n−1 1

k!

1

1

1

= n! 1 + + · · · +

\+

= n!

.

2!

(n − 2)! (n − 1)!

k=1

It is possible to write an analytical expression for T (n) by non-elementary

functions, however, for solution of the posed problem it is enough to evaluate the

asymptotic behaviour of the function T (n).

Note that for n → ∞

n−1 1

` `1

∞

` `1

∞

lim

\=

\=

− 1 = e − 1,

n→∞

k

!

k!

k!

k=1

k=1

k=0

where e = 2.71828 . . . is the base of natural logarithms. Hence we obtain the

inequality

n−1 1

n!  n!

` `(e − 1)n!,

k!

k=1

and, ﬁnally, T (n) = O(n!).





Answers and Solutions

89

[**2.25**](#br83)[** ](#br83)Solution.

n−1 1

According to the result of the previous problem, T (n) = n!

.

k!

k=1

Let us expand the expression en(n, 1) − n!, taking into account the deﬁnition

of incomplete gamma function:

n−1 1k

k!

n

k=0

−1

` `1

n−1

1

en(n, 1) − n! = en · (n − 1)! e−1

− n! = n!

− n! = n!

,

k!

k!

k=0

k=1

which coincides with T (n).

[**2.26**](#br83)[** ](#br83)Solution.

Let us ﬁnd the total number of inversions S(N) contained in all permutations of

S(N)

N elements. The relation

will be equal to the mean value of the number of

N!

inversions A(N) in the N-element array.

In order to compute the variable S(N) suppose that some permutation

(a , a , . . . , a , a ) contains exactly σ inversions.

i1

i2

i −1

i

n

n

Note that in the permutation (a , a , . . . , a , a ) the number of inversions is

i

n

in−1

i2

i1

N(N − 1)

− σ. This means that the total number of inversions in the pair of arrays

2

(a , a , . . . , a , a ) and (a , a , . . . , a , a )

i1

i2

in−1

i

n

i

n

in−1

i2

i1

$

%

N(N − 1)

N(N − 1)

is equal to σ +

− σ

\=

.

2

2

Since there exist only N! permutations of the N-element array, then S(N) =

1

2

N(N − 1)

N! ×

, and therefore there exists the following estimate of the mean

2

value of the number of inversions:

S(N)

N!

1

4

A(N) =

\=

N2 + O(N) for N → ∞.

[**2.27**](#br83)[** ](#br83)Proof.

Denote the elements of the matrix B by b , 1  i, j  n. Using the introduced

ij

designation, we can write that the matrix I + εB is formed by the elements (δ

\+

ij

εb ).

ij

According to the deﬁnition, the variable det(I + εB) is equal to the sum over all

possible permutations:

det(I + εB) =

(−1)σ (δ1i1 + εb1i1 )(δ2i2 + εb2i2 ) . . . (δnin + εbni ).

n

perm





90

2 Matrix Algebra

Removing the brackets under the summation sign, we obtain

det(I + εB) =

(−1)σ (δ1i1δ2i2 . . . δnin

perm

\+ εb1i1 δ2i2 δ3i3 . . . δnin

\+ εb2i2 δ1i1 δ3i3 . . . δnin

\+ εb3i3 δ1i1 δ2i2 . . . δnin + · · ·

\+ εb

. . . δ(n−1)in−1

nin δ1i1 δ2i2

\+ ε2(. . . ) + · · · ).

The product δ1i1 δ2i2 . . . δnin is equal to one, if i = 1, i = 2, ..., i = n, and is

1

2

n

equal to zero in other cases.

Further, the products of the form

εbkik δ1i1 δ2i2 . . . δ

δ

. . . δnin

(k−1)ik−1 (k+1)ik+1

reduce to the summands εbkk.

This implies that


2

det(I + εB) = (−1)σ0 1 + εb11 + εb22 + · · · + εbnn + O(ε ) ,

where σ0 is the number of inversions in the permutation (i , i , . . . , i )

\=

1

2

n

(1, 2, . . ., n).

It is clear that σ = 0.

0

As a result we obtain

$

n

%

2

2

det(I + εB) = (−1)σ0 1 + ε

bkk + O(ε ) = 1 + ε tr B + O(ε ).

k=1


I

[**2.28**](#br83)[** ](#br83)Answer: det

[**2.29**](#br83)[** ](#br83)Proof.

= 1 − pε(tr B) + O(ε2).

(I + εB)p





Answers and Solutions

91

Represent the matrix M in the form M = G(I + εG−1H). Calculate the

determinant

det M = det G det(I + εG−1H)

$

∞

−1

)

%

` `−1 k

(

= det G exp(tr ln(I + εG−1H)) = det G exp tr

(εG−1H)k

k

k=1

1

= det G 1 + εtr (G−1H) + ε (tr (G−1H) − tr (G−1H) ) + O(ε ) .

2

2

2

3

2

Thus, the formula ([2.80](#br83)) is proved.

[**2.30**](#br83)[** ](#br83)Solution.

The determinant of the matrix is equal to det A = ad − bc.

Calculate the cofactors for each of the elements of the matrix A:

A11 = (−1)1+1 · d = d, A12 = (−1)1+2 · c = −c;

A21 = (−1)2+1 · b = −b, A22 = (−1)2+2 · a = a.

Write a matrix of cofactors:

⎡

⎣

⎤

⎦

d −c

−b a

.

Then the sought inverse matrix will have the form:

⎡

⎣

⎤

1

−

c a

d

b

A−1

\=

⎦

.

ad − bc

−

[**2.31**](#br84)[** ](#br84)Solution.

(1) Since det A = −2 = 0, then the inverse matrix exists. Find the cofactors of the

elements of the matrix A:

A11 = 4,

A21 = −2,

A12 = −3,

A22 = 1.

⎡

⎤

4 −3

−2 1

Therefore, the matrix of cofactors can be written in the form: ⎣

⎦ .





92

2 Matrix Algebra

⎡

⎤

⎦

⎡

⎤

T

4 −3

−2 1

4 −2

−3 1

Transpose the matrix (A ): ⎣

= ⎣

⎦ .

ij

For computing A−1, divide the obtained adjoint matrix by the determinant:

⎡

⎤

⎡

⎤

4 −2

−3 1

−2

3/2 −1/2

1

⎦

−2 = ⎣

⎦

A

−1 = ⎣

/(

)

.

(2) Since det A = 1 = 0, then the inverse matrix exists. Find the cofactors of the

elements of the matrix A:

A11 = 7, A12 = −5,

A21 = −4, A22 = 3.

⎡

⎤

⎡

⎤

T

7 −5

−4 3

7 −4

−5 3

Transpose the matrix (A ): ⎣

⎦

= ⎣

⎦ .

ij

⎡

⎤

⎡

⎤

1

7 −4

−5 3

7 −4

−5 3

Therefore, A−1 =

⎣

⎦ = ⎣

⎦ .

det A

(3) Compute the determinant by the method of expansion in the ﬁrst column:












−3 1 

−4 5 

−4 5

det A = 3 

` `− 2 

` `+ 3 

` `= 24 − 58 + 33 = −1 = 0.






−5 −1

−5 −1

−3 1

Find the cofactors:




−3 1 

A11 =

` `= 8

, A12

= 5, A13 = −1

,


−5 −1

A21 = −29, A22 = −18, A23 = 3,

A31 = 11, A32 = 7, A33 = −1.

⎡

⎤

8

5

−1

⎢

⎥

We will obtain the matrix of cofactors: ⎢−29 −18 3 ⎥ .

⎣

⎡

⎦

11

7

−1

Perform the transposition operation:

⎡

⎤

⎤

T

8

5

−1

8 −29 11

5 −18 7

⎢

⎥

⎢

⎥

⎢

⎥

= ⎢

⎥

−29 −18 3

.

⎣

⎦

⎣

⎦

11

7

−1

−1

3

−1





Answers and Solutions

93

With the help of division by det A write the inverse matrix:

⎡

⎤

⎡

⎤

8 −29 11

5 −18 7

−8 29 −11

−5 18 −7

1

⎢

⎥

⎢

⎥

A−1

\=

⎢

⎥

\=

⎢

⎥

.

⎣

⎦

⎣

⎦

det A

−1

3

−1

1 −3

1

(4) Since det A = −3 = 0, then A−1 is determined. Find the cofactors Aij :

A11 = 7, A12 = −5, A13 = 6,

A21 = −6, A22 = 3, A23 = −3,

A31 = 1, A32 = 1, A33 = −3.

⎡

⎤

7 −6 1

1

⎢

⎥

The inverse matrix is equal to A−1

\=

⎢−5 3 1 ⎥

\=

⎣

⎦

det A

6 −3 −3

⎡

⎣

⎤

7

1

−

2 −

⎢

3

3⎥

⎢ 5

1⎥

⎢

−1 − ⎥ .

⎦

3

3

1

−2 1

(5) Find the determinant: det A = −27 = 0. The cofactors are equal to

A11 = −3, A12 = −6, A13 = −6,

A21 = −6, A22 = −3, A23 = 6,

A31 = −6, A32 = 6, A33 = −3.

Compute the elements of the inverse matrix:

⎡

⎤

⎡

⎤

−3 −6 −6

−6 −3 6

−6 6 −3

1 2

2

1

⎢

⎥

1 ⎢

⎥

A−1

\=

⎢

⎥

\=

⎢

⎥

.

2 1 −2

⎣

⎦

⎣

⎦

det A

9

2 −2 1





94

2

Matrix Algebra

[**2.32**](#br84)[** ](#br84)Answer:

⎡

⎢

⎤

⎥

1

2

1 −

0

0

⎡

⎤

1

2

1 −

0

⎡

⎤

⎢

⎥

1

1

1

⎢

⎥

⎢

⎥

1 −

⎢

⎥

⎢0

−

0 ⎥

1

1

⎢

2⎥

⎢

⎥

⎢

2

3

1

⎥

(1) ⎣

⎦ ; (2) ⎢0

− ⎥ ; (3) ⎢

⎥ .

1

1

⎢

2

3⎥

⎢

⎥

0

⎣

⎦

⎢0 0

− ⎥

1

3

2

⎢

3

4⎥

0 0

⎣

⎦

1

0 0

0

4

[**2.33**](#br84)[** ](#br84)Answer: [A, A−1] = [A, A−1] = O.

[**2.34**](#br84)[** ](#br84)Solution.

(1) As is known, the matrix A does not have the inverse one when the condition

det A = 0 is fulﬁlled.





−1 λ λ




Calculate the determinant: 

0 = −λ − 3λ = −λ (λ + 3).

3

2

2

` `λ λ 

` `6 4 

λ

Therefore, the matrix does not have the inverse one for λ ∈ {0, −3}.

(2) The determinant is equal to −λ3 + 3λ2 + λ − 3 = −(λ − 3)(λ − 1)(λ + 1). The

matrix does not have the inverse one for λ ∈ {−1, 1, 3}.

[**2.35**](#br84)[** ](#br84)Solution.

For ﬁnding the inverse matrix, compute the determinant det A.




1 α 0 0

0 1 β 0

0 0 1 γ








det A =

,








0 0 0 1

det A = 1, since A is the upper triangular matrix and the determinant is equal to the

product of the diagonal elements.

Find the cofactors:

A11 = 1, A12 = 0, A13 = 0, A14 = 0,

A21 = −α, A22 = 1, A23 = 0, A24 = 0,

A31 = αβ, A32 = −β, A33 = 1, A34 = 0,

A41 = −αβγ , A42 = βγ, A43 = −γ, A44 = 1.





Answers and Solutions

95

We perform transposition and obtain the adjoint matrix:

⎡

⎤

⎡

⎤

T

1

0

1

0 0

1 −α αβ −αβγ

0 1 −β βγ

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

−α

0 0

⎢

⎥

⎢

⎥

\=

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

αβ −β 1 0

−αβγ βγ −γ 1

0 0

1

−γ

⎣

⎦

⎣

⎦

0 0

0

1

Since the determinant is equal to one, then A−1 coincides with the adjoint matrix:

⎡

⎤

1 −α αβ −αβγ

0 1 −β βγ

⎢

⎥

⎢

⎥

⎢

⎥

A−1 = ⎢

⎥ .

⎢

⎥

0 0

1

−γ

⎣

⎦

0 0

0

1

As is shown above, the determinant det A does not depend on the parameters

α, β, γ . Therefore, the matrix A−1 is deﬁned for any values of α, β, γ

∈ R.

[**2.36**](#br85)[** ](#br85)Solution.

The determinant of the matrix G = (g ) is equal to det G = (−1)n(n−1)/2,

n

ij

n

since non-zero product in the sum of the form ([2.5](#br60)) is equal to g1,n

1, and the multiplier σ for this product takes the value σ = (−1)n(n

g

2,n−1

. . . g

−1)/2

\=

n,1

(see

Problem [**2.5**](#br79)).

Construct the matrix of cofactors of the elements g , where 1  i, j  n. The

ij

cofactor of any element equal to zero will be equal to zero. This follows from the

fact that in case of deletion of the non-zero element in the corresponding minor

appears a zero row and a zero column, and, in turn, such a minor is equal to zero.

The minor of any element g

, located on the secondary diagonal, will be

, since after deletion of gi,(n+1)−i we will

i,(n+1)−i

−1)(n−2)/2

equal to det G

obtain the matrix G

= (−1)(n

n−1

of size (n − 1) × (n − 1).

n−1

Therefore, cofactors of such elements g

are equal to

i,n−i

(−1)i+(n+1−i) · det Gn−1

= −1 n+1 · −1 (n−1)(n−2)/2

(

)

(

)

= (−1)n(n−1)/2+2 = (−1)n(n−1)/2

.

Thus, the matrix of cofactors is equal to the original G , multiplied by

n

(−1)

n(n−1)/2.

As is easy to see, transposition does not change the obtained matrix. The last

step—divide the adjoint matrix by the determinant det G = (−1)n(n−1)/2. Finally

n

we obtain that the matrix inverse of G coincides with it itself: G−1 ≡ G for all

values of n  2.





96

2 Matrix Algebra

[**2.37**](#br85)[** ](#br85)Solution.

Let us provide a code in Python for solution of the problem.

import numpy as np

def get\_Hilbert\_matrix(n):

return np.matrix([[ 1 / (i + j - 1)

for j in range(1, n + 1)] for i in range(1, n + 1)])

matrix = get\_Hilbert\_matrix(6)

inversed = np.linalg.inv(matrix)

hh1 = np.matmul(matrix, inversed)

h1h = np.matmul(inversed, matrix)

print(matrix)

print(inversed)

print(hh1)

print(h1h)

The difference of the elements of the matrices H · H−1 and H−1 · H computed

with the help of Python from the identity matrix is ∼ 10−10 for n = 6, ∼ 10−7 for

n = 8 and ∼ 10

−8 for = 7. (Here, the symbol ∼ means equality by the order of

n

value.)

Thus, Hilbert matrices demonstrate [accumulation](#br422)[ ](#br422)of machine errors when mak-

ing computations with real numbers [[58](#br422)[\].](#br422)[ ](#br422)These matrices are very often used for

testing of numerical algorithms.

The matrix H−1 [can](#br421)[ ](#br421)[be](#br421)[ ](#br421)found in an explicit form; the analytical representations

for hij are shown in [[40](#br421)[\]](#br421). An interesting peculiarity of this problem is also the fact

that the elements of the inverse matrix are integer numbers.

[**2.38**](#br85)[** ](#br85)Solution.

This matrix is an upper triangular one, and its determinant is equal to the product

of the elements positioned on the main diagonal, i.e. is equal to one.

Construct the matrix of cofactors. The cofactors of all unit elements positioned

on the main diagonal will be equal to one. Upon deleting all zeroes except

those standing on the diagonal below the main one, there appear matrices with

proportional rows, therefore, their minors will be equal to zero. Those zeroes that

are positioned on the diagonal below the main one, as cofactors will have the values

(−λ). The sum i + j for such elements is always odd, since they are positioned

below the main diagonal, and upon their deletion we obtain an upper triangular

matrix with one element λ and other unities on the main diagonal. Upon deletion of

λ of any degree, except zero, we obtain an upper triangular matrix with zeroes and

unities on the main diagonal. Therefore, both the minor and the cofactor are in this

case equal to zero.





Answers and Solutions

97

Finally, having executed the transposition operation, we obtain the inverse

matrix:

⎡

⎤

1 −λ 0 0 . . . 0

0 1 −λ 0 . . . 0

0 0 1 −λ . . . 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

.

⎢

⎥

⎢

⎥

⎢ . . . . . . . . . . . . . . . . . ⎥

⎣

⎦

0 0

0

0 . . . 1

[**2.39**](#br85)[** ](#br85)Solution.

Let us use mathematical induction method.

B a s i s s t e p

For the least natural n = 1 we have

(A1)−1 = A−1 1 is true.

I n d u c t i v e s t e p

Assume that for n = k the equality

−1

−1 −1

−1 −1

. . . A A

2 1

(A1A2 . . . A −1A ) = A

A

k

k

−1

k

k

is valid. Then we should prove that for n = k + 1 the following is true:

−1

−1

−1

k

−1 −1

(A1A2 . . . A +1−1A +1) = A

A

. . . A

A

.

1

k

k

+1

+1−1

2

k

−1

−1

1

Denote the expression for Ak . . . A by B, Then:

(BAk+1)−1 = A B−1 = A (A

−1

−1

−1 −1

A

k

. . . A ).

−1

k

+1

k

+1

k

−1

1

Therefore, according to the mathematical induction method, ∀n ∈ N the identity

−1

−1 −1

−1 −1

. . . A A

2 1

(A1A2 . . . A −1A ) = A

A

n

n

n

−1

n

is valid.

[**2.40**](#br85)[** ](#br85)Solution.

⎡

⎤

2 1

(1) Find the matrix inverse of the matrix A = ⎣ ⎦.

0 2

Its determinant is equal to det A = 4, the matrix of cofactors has the

⎡

⎤

⎡

⎤

2 0

1/2 −1/4

components ⎣

⎦ , inverse of the matrix: A

−1

\=

⎣

⎦

.

−1 2

0

1/2





98

2 Matrix Algebra

⎡

⎤

−6 4

We obtain the matrix X by multiplying A−1 by the matrix B = ⎣

⎦:

2 1

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

⎦

1/2 −1/4

−6 4

−7/2 7/4

1

4

−14 7

4 2

X =

⎣

⎦ · ⎣

⎦ = ⎣

⎦ =

⎣

.

0

1/2

2 1

1

1/2

⎡

⎤

−1 1 1

⎢

⎥

(2) Let us ﬁnd the matrix inverse of the matrix A = ⎢ 0 2 2⎥.

⎣

⎤

⎦

0 2 3

The determinant is equal to det A = −2.

−1

The inverse of the matrix A

:

⎡

−1 1/2 0

0 3/2 −1

0 −1 1

⎢

⎥

A−1

\=

⎢

⎥

.

⎣

⎦

Multiply the matrix inverse of the matrix A by the matrix

⎡

⎤

−2 1 1

⎢

⎥

B = −1 0 2

⎢

⎥:

⎣

⎦

−1 −2 0

⎡

⎤ ⎡

⎤

⎡

⎤

−1 1/2 0

−2 1 1

−1 0 2

−1 −2 0

3 −2 0

⎢

⎥ ⎢

⎥

1 ⎢

⎥

X = A−1B = 0 3/2 −1

⎢

⎥ ⎢

⎥

\=

⎢

⎥

.

−1 4

6

⎣

⎦ ⎣

⎦

⎣

⎦

2

0 −1 1

0 −4 −4

(3) We obtain the solution of the equation multiplying both sides of the equation

X · A = B by A

−1 on the right.

To do this, ﬁnd the matrix inverse of the matrix A:

⎡

⎤

−30 12 38

−5 3 7

−30 14 36

1 ⎢

⎥

A−1

\=

⎢

⎥

.

⎣

⎦

10





Answers and Solutions

99

Compute the elements of an unknown matrix X = B · A−1

:

⎡

⎤

⎡

⎤

⎡

⎤

0 −1 2

−30 12 38

−5 3 7

−30 14 36

−55 25 65

100 −46 −124

−305 143 367

⎢

⎥

1 ⎢

⎥

1 ⎢

⎥

X = −1 −2 −2

⎢

⎥ ·

⎢

⎥ =

⎢

⎥

.

⎣

⎦

⎣

⎦

⎣

⎦

10

10

0

1 10

(4) From the equation A · X · B = C, ﬁnd the unknown matrix X by the formula

X = A

−1 ·

·

−1.

C B

We have

⎡

⎣

⎤

⎦

⎡

⎣

⎤

⎦

1

2 −3

1

−4 7

5 −1

A−1

\=

,

B−1

\=

.

13

31

3 2

Consecutively perform multiplications in the following order:

(A−1 · C) · B−1

.

Multiply the matrix inverse of the matrix A by the matrix C:

⎡

⎤ ⎡

⎤

⎡

⎤

1

2 −3

3 2

1 −1

0 1

1

2 −5

3 −1

A−1C =

⎣

⎦ ⎣

⎦

\=

⎣

⎦

.

13

13

Finally, multiply the product A−1C by the matrix, inverse of the matrix B:

⎡

⎤

⎡

⎤

⎡

⎤

1

2 −5

3 −1

1

−4 7

5 −1

1

−33 19

−17 22

X =

⎣

⎦ ·

⎣

⎦ =

⎣

⎦

.

13

31

403

⎡

⎤

1

0

1

0

⎢

⎥

[**2.41**](#br86)[** ](#br86)Answer: ⎢

⎥.

0

0

⎣

⎦

0 256a 1





100

2 Matrix Algebra

[**2.42**](#br86)[** ](#br86)Solution.

Having calculated the several ﬁrst powers Ak, namely the second, third, fourth

⎡

⎤

1 0 0

⎢

⎥

and ﬁfth powers of the matrix A = ⎢ 1 1⎥, we have

g

⎣

⎦

h 0 1

⎡

⎤

⎡

⎤

1

0 0

1

0 0

⎢

⎥

⎢

⎥

A2 = 2g + h 1 2

⎢

⎥

,

,

A3 = 3g + 3h 1 3

⎢

⎥

,

⎣

⎦

⎤

⎣

⎡

⎦

2h 0 1

3h 0 1

⎡

⎤

1

0 0

1

0 0

⎢

⎥

⎢

⎥

A4 = 4g + 6h 1 4

⎢

⎥

A5 = 5g + 10h 1 5

⎢

⎥

.

⎣

⎦

⎣

⎦

4h 0 1

5h

0 1

Based on the obtained equalities, suppose that for all natural values of n the

identity is fulﬁlled:

⎡

⎤

n

1

0 0

⎢

⎥

A

n = ⎢

ng + n(n − 1)h/2 1 n

⎥

,

⎣

⎦

nh

0 1

denote the respective predicate by P (n).

Let us use the mathematical induction method.

B a s i s s t e p

⎡

⎤

1

0 0

⎢

⎥

A1 = 1 · g + 1(1 − 1)h/2 1 1 = A is true.

⎢

⎥

⎣

⎦

1 · h

0 1

I n d u c t i v e s t e p

Assume that for n = k the predicate P (n) takes the true value, Then:

⎡

⎤

1

0 0

⎢

⎥

A

k = ⎢

kg + k(k − 1)h/2 1 k

⎥

.

⎣

⎦

kh

0 1





Answers and Solutions

101

Prove that for n = k + 1 the equality is valid:

⎡

⎤

1

0

0

⎢

⎥

A

k+1 = ⎢ + 1

(k

)g k(k

\+

(k + 1)h

\+ 1 2 1 + 1⎥

)h/

k

.

⎣

⎡

⎦

0

1

Indeed,

⎤ ⎡

⎤

1

0 0

1 0 0

g 1 1

h 0 1

⎢

⎥ ⎢

⎥

k+1 = ⎢

⎥ ⎢

⎥

A

kg + k(k − 1)h/2 1 k

⎣

⎡

⎦ ⎣

⎦

kh

0 1

⎤

1

0

0

⎢

⎥

= ⎢ + 1

\+ 1 2 1 + 1⎥ .

(k

)g k(k

\+

(k + 1)h

)h/

k

⎣

⎦

0

1

Thus, the predicate P (n) is proved for all n ∈ N.

Substituting as the exponent of the matrix the number n = 512, we obtain the

⎡

⎤

1

0 0

⎢

⎥

answer: A512 = ⎢256 2 + 511 1 512⎥ .

( g

h)

⎣

⎦

512h

0 1

[**2.43**](#br86)[** ](#br86)Solution.

⎡

⎤

Fn−1

F

Denote by P (n) the predicate Fn = ⎣

n ⎦

.

Fn F +1

n

B a s i s s t e p

The basis step is formed by the statement P(2):

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

⎦

0 1

0 1

1 1

F1 F2

F2 F3

⎣

⎦ ⎣ [⎦](#br86)[ ](#br86)= ⎣ ⎦ = ⎣

,

1 1

1 1

1 2

which corresponds to the formula ([2.85](#br86)).

I n d u c t i v e s t e p

Assume that for n = k the statement is true:

⎡

⎤

Fk−1

F

k = ⎣

k ⎦

.

F

Fk F +1

k





102

2

Matrix Algebra

Compute the matrix Fn for n = k + 1:

⎡

⎤ ⎡

⎤

⎦

⎡

⎣

⎤

F

k ⎦ ⎣0 1

Fk Fk−1 + F

Fk−1

k+1 = ⎣

\=

k⎦

.

F

Fk F +1

1 1

F +1 F + F +1

k

k

k

k

According to the deﬁnition of the Fibonacci sequence, each element of this

sequence is equal to the sum of two previous ones, and for all k > 1 the identity

F −1 + F = F +1 is valid.

k

k

k

Thus, the predicate P (n) is proved for all natural n > 1.

[**2.44**](#br86)[** ](#br86)Solution.

Let us try to ﬁnd regularity in the sequence A1, A2, A3, . . . . To do this, raise the

matrix to the second, third and fourth powers:

⎡

⎤ ⎡

⎤

⎡

⎤

1 α γ

1 α γ

0 1 β

0 0 1

1 2α 2γ + αβ

⎢

⎥ ⎢

⎥

⎢

⎥

A2 = 0 1 β

⎢

⎥ ⎢

⎥

\=

⎢

⎥

,

0 1

2β

⎣

⎡

⎦ ⎣

⎦

⎣

⎦

0 0 1

0 0

1

⎤ ⎡

⎤

⎡

⎤

1 2α 2γ + αβ

1 α γ

0 1 β

0 0 1

1 3α 3γ + 3αβ

⎢

⎥ ⎢

⎥

⎢

⎥

3

2

⎢

⎥ ⎢

⎥

⎢

⎥

A = A · A = 0 1

2β

\=

0 1

3β

,

⎣

⎦ ⎣

⎦

⎣

⎦

0 0

1

0 0

1

⎡

⎤ ⎡

⎤

⎡

⎤

1 3α 3γ + 3αβ

⎣

1 α γ

0 1 β

0 0 1

1 4α 4γ + 6αβ

⎢

⎥ ⎢

⎥

⎢

⎥

4

3

⎢

⎥ ⎢

⎥

⎢

⎥

A = A · A = 0 1

3β

\=

0 1

4β

.

⎦ ⎣

⎦

⎣

⎦

0 0

1

0 0

1

1

2

3

Analysis of the sequence of the powers A , A , A , . . . leads to a hypothesis that

⎡

⎤

1 nα nγ + n(n − 1)αβ/2

⎢

⎥

⎥

A

n = ⎢0 1

nβ

.

⎣

⎦

0 0

1

Let us prove the truth of this supposition with the help of the mathematical

induction method.

⎡

⎤

1 nα nγ + n(n − 1)αβ/2

⎢

⎥

Denote by P (n) the statement “An = ⎢0 1

⎥”.

nβ

⎣

⎦

0 0

1

B a s i s s t e p

The truth of the statement P(1) is obvious.





Answers and Solutions

103

I n d u c t i v e s t e p

Assume that P (n) is valid for n = k for some k  1:

⎡

⎤

1 kα kγ + k(k − 1)αβ/2

⎢

⎥

k = ⎢

⎥

.

A

0 1

kβ

⎣

⎦

0 0

1

Prove that P (k) ⇒ P(k + 1).

⎡

⎤ ⎡

⎤

1 kα kγ + k(k − 1)αβ/2

1 α γ

0 1 β

0 0 1

⎢

⎥ ⎢

⎥

Ak+1 = Ak ·

A

= ⎢

⎥ ⎢

⎥

0 1

kβ

⎣

⎦ ⎣

⎦

0 0

1

⎡

⎤

1 (k + 1)α (k + 1)γ + k(k + 1)αβ/2

⎢

⎥

= ⎢0

⎥ .

1

(k

\+ 1

1

)β

⎣

⎦

0

0

Therefore, P (n) takes the true value for all n  1. Thus it is proved that

⎡

⎤

1 nα nγ + n(n − 1)αβ/2

⎢

⎥

n = ⎢

⎥

A

0 1

nβ

⎣

⎦

0 0

1

for all n ∈ N.

[**2.45**](#br87)[** ](#br87)Solution.

Assume that q-th power of the matrix U(ϕ) is determined by the formula:

⎡

⎤

cos(qϕ) sin(qϕ)

− sin(qϕ) cos(qϕ)

q = ⎣

⎦

,

where ∈ Z

q

.

(U(ϕ))

Denote this statement by P (q) and prove it ﬁrst for q ∈ N. Let us apply the

mathematical induction method.

B a s i s s t e p

For n = 1 we have

⎡

⎤

⎦

cos(ϕ) sin(ϕ)

− sin(ϕ) cos(ϕ)

(U(ϕ))1 =

⎣

= U(1 · ϕ) is true.





104

2

Matrix Algebra

I n d u c t i v e s t e p

Assume that P (n) is true for n = k:

⎡

⎤

⎦

cos(kϕ) sin(kϕ)

− sin(kϕ) cos(kϕ)

(U(ϕ))

k = ⎣

.

Prove the truth of the statement for n = k + 1.

⎡

⎤ ⎡

⎤

⎦

cos(kϕ) sin(kϕ)

− sin(kϕ) cos(kϕ)

cos ϕ sin ϕ

− sin ϕ cos ϕ

(U(ϕ))k+1 = ⎣

⎦ ⎣

⎡

⎤

cos(kϕ) cos ϕ − sin(kϕ) sin ϕ cos(kϕ) sin ϕ + sin(kϕ) cos ϕ

− sin(kϕ) cos ϕ − cos(kϕ) sin ϕ − sin(kϕ) sin ϕ + cos(kϕ) cos ϕ

= ⎣

⎦

⎡

⎤

cos(k + 1)ϕ sin(k + 1)ϕ

− sin(k + 1)ϕ cos(k + 1)ϕ

= ⎣

⎦ .

Therefore, for q ∈ N there exists the equality:

⎡

⎤

⎦

cos(qϕ) sin(qϕ)

(U(ϕ))

q = ⎣

.

− sin(qϕ) cos(qϕ)

Now it only remains for us to prove the truth of this equality for all integer q.

Indeed, (U(ϕ))0 = I = U(0) and for all ϕ ∈ R there exists the inverse matrix

U(ϕ)−1 = U(−ϕ).

Thus, for q = 0, 1, 2, . . . the equality (U(ϕ))−q = U(−qϕ) is valid.

This means that

⎡

⎤

cos(qϕ) sin(qϕ)

− sin(qϕ) cos(qϕ)

q = ⎣

⎦ for ∈ Z

q

.

(U(ϕ))

[**2.46**](#br87)[** ](#br87)Answer:

[A, Bq] = qBq−1 for all q ∈ Z.





Answers and Solutions

105

[**2.47**](#br87)[** ](#br87)Solution.

Consecutively perform the algebraic operations:

(1)

⎡

⎣

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

⎦

1 0

1 0

1 0

1 0

f (A) =

⎦ ⎣ ⎦ − 3 ⎣ ⎦ + 2 ⎣

0 1

0 1

0 1

0 1

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

1 0

3 0

2 0

0 0

= ⎣ ⎦ − ⎣ ⎦ + ⎣ ⎦ = ⎣ ⎦ .

0 1

0 3

0 2

0 0

(2)

⎡

⎣

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

⎦

1 −2

1 −2

1 −2

1 0

7 −4

−6 7

f (A) =

⎦ ⎣

⎦ − 3 ⎣

⎦ + 2 ⎣ ⎦ = ⎣

−3 1

−3 1

−3 1

0 1

⎡

⎤

⎡

⎤

⎡

⎤

3 −6

−9 3

2 0

6 2

− ⎣

⎦ + ⎣ ⎦ = ⎣ ⎦ .

0 2

3 6

[**2.48**](#br87)[** ](#br87)Solution.

(1)

⎡

⎤ ⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

1 0 0

1 0 0

1 0 0

1 1 0

1 1 1

1 0 0

1 1 0

1 1 1

1 0 0

⎢

⎥ ⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥

g(A) = 1 1 0

⎥ ⎢

⎢

⎥ ⎢

⎥ + ⎢

⎥ − 3 ⎢

⎥

1 1 0

0 1 0

⎣

⎡

⎦ ⎣

⎤

⎦ ⎣

⎦

⎣

⎤

⎦

⎣

⎦

1 1 1

1 1 1

0 0 1

⎡

⎤

⎡

⎡

⎤

1 0 0

1 0 0

3 0 0

−1 0

⎣

0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

= ⎢3 1 0⎥ + ⎢1 1 0⎥ − ⎢0 3 0⎥ = ⎢ 4 −1 0 ⎥ ;

⎣

⎦

⎣

⎦

⎣

⎦

⎦

6 3 1

1 1 1

0 0 3

7

4 −1

(2)

⎡

⎤ ⎡

⎤ ⎡

⎤

−2 1 0

−2 1 0

3 −1 1

−2 1 0

3 −1 1

⎢

⎥ ⎢

⎥ ⎢

⎥

g(A) = 3 −1 1

⎢

⎥ ⎢

⎥ ⎢

⎥

⎣

⎦ ⎣

⎦ ⎣

⎦

2

1 0

2

1 0

2

1 0





106

2

Matrix Algebra

⎡

⎤

⎡

⎤

−2 1 0

1 0 0

⎢

⎥

⎢

⎥

\+ ⎢ 3 −1 1⎥ − 3 ⎢0 1 0⎥

⎣

⎦

⎣

⎦

2

1 0

0 0 1

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

−21 11 −3

−2 1 0

3 0 0

−26 12 −3

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

= ⎢ 27 −13 5 ⎥ + ⎢ 3 −1 1⎥ − ⎢0 3 0⎥ = ⎢ 30 −17 6 ⎥ .

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

7

−1

1

2

1 0

0 0 3

9

0

−2

[**2.49**](#br87)[** ](#br87)Solution.

(1) The numerator of the fraction is equal to

⎡

⎤

1

0

0

⎢

⎥

⎢

⎥

0 −41 0

0

.

⎣

⎦

0

−6

In turn, the denominator forms the matrix

⎡

⎤

−4

0

0

⎢

⎥

⎢

⎥

0 −46 0

,

⎣

⎦

0

0

−6

and the matrix that is inverse of it is equal to

⎡

⎤

−1/4

0

−1/46

0

0

0

⎢

⎥

⎢

⎥

0

.

⎣

⎦

0

−1/6

Having performed the multiplication operation, we obtain

⎡

⎤ ⎡

⎤

⎡

⎤

1

0

0

−1/4

0

−1/46

0

0

0

−23 0 0

⎢

⎥ ⎢

⎥

⎢

⎥

g(A) = 0 −41 0

⎢

⎥ ⎢

0

⎥ = 1 92 ⎢

/

0

82 0

⎥

.

⎣

⎦ ⎣

⎦

⎣

⎦

0

0

−6

0

−1/6

0

0 92





Answers and Solutions

107

(2) The numerator of the fraction is equal to

⎡

⎤

−6 2

0

⎢

⎥

⎢

⎥

0 −6 0

.

⎣

⎦

0

2 −6

The denominator of this fraction is equal to

⎡

⎤

−6 −2 0

0 −6 0

0 −2 −6

⎢

⎥

⎢

⎥

.

⎣

⎦

Let us ﬁnd the matrix inverse of the denominator:

⎡

⎤

−1/6 1/18

0

0

⎢

⎥

⎢

⎥

0

−1/6

.

⎣

⎦

0

1/18 −1/6

As a result we obtain

⎡

⎤ ⎡

⎤

⎡

⎤

−6 2

0

−1/6 1/18

0

0

3 −2 0

0 3 0

0 −2 3

⎢

⎥ ⎢

⎥

1 ⎢

⎥

g(A) = 0 −6 0

⎢

⎥ ⎢

0

−1/6

⎥ =

⎢

⎥

.

⎣

⎦ ⎣

⎦

⎣

⎦

3

0

2 −6

0

1/18 −1/6

[**2.50**](#br88)[** ](#br88)Proof.

Let us consider the sequence of integer non-negative powers of the matrix A =

⎡

⎤

0 −1

⎣

⎦:

1 0

⎡

⎣

⎤

⎦

⎡

⎣

⎤

⎦

⎡

⎣

⎤

⎦

1 0

0 1

0 −1

−1 0

0 −1

A0 =

, A1 =

, A2 =

,

1 0

⎡

⎤

⎡

⎤

0 1

1 0

A3 =

⎣

⎦

, A4 =

⎣

⎦

and so on.

−1 0

0 1





108

2 Matrix Algebra

Therefore, the elements of the matrix exp(A) are deﬁned by the sums

∞

` `−1 k

(

)

(eA)11

= 1 + 0 1! − 1 2! + 0 3! + 1 4! + · · · =

/

/

/

/

= cos 1

,

(2k)!

k=0

∞

` `−1 k+1

(

)

(eA)12

(eA)21

(eA)22

= 0 − 1 1! − 0 2! + 1 3! + 0 4! + · · · =

/

/

/

/

= − sin 1

= sin 1

,

(2k + 1)!

k=0

∞

−1 k

(

)

= 0 + 1 1! + 0 2! − 1 3! + 0 4! + · · · =

/

/

/

/

,

(2k + 1)!

k=0

∞

` `−1 k

(

)

= 1 + 0 1! − 1 2! + 0 3! − 1 4! + · · · =

/

/

/

/

= cos 1

.

(2k)!

k=0

Therefore, there exists the equality

⎡

⎤

cos 1 − sin 1

sin 1 cos 1

exp(A) = ⎣

⎦ .

[**2.51**](#br88)[** ](#br88)Solution.

(1) Compute the lower powers of the matrix A:

⎡

⎤

⎡

⎤

⎡

⎤

1 0 0

1 0 0

1 0 0

⎢

⎥

⎢

⎥

⎢

⎥

A0 = 0 1 0

⎢

⎥

,

A1 = 0 1 0

⎢

⎥

,

A2 = 0 1 0

⎢

⎥

.

⎣

⎦

⎣

⎦

⎣

⎦

0 0 1

0 0 0

0 0 0

It is clear that ∀n  1 (An = A). The elements of the matrix exp(A) are

equal to

1

1

1

(eA)11

\=

(eA)22

= 1 +

\+

\+

\+ · · · =

e, (eA)33

= 1

,

1! 2! 3!

and the remaining elements take zero values.

Therefore,

⎡

⎤

e 0 0

⎢

⎥

⎦

exp(A) = ⎢0 0⎥ .

e

⎣

0 0 1





Answers and Solutions

109

(2) The lower powers of the matrix are equal to

⎡

⎤

⎡

⎤

⎡

⎤

1 0 0

0 1 0

0 0 1

⎢

⎥

⎢

⎥

⎢

⎥

A0 = 0 1 0

⎢

⎥

,

A1 = 0 0 1

⎢

⎥

,

A2 = 0 0 0

⎢

⎥

.

⎣

⎦

⎣

⎦

⎣

⎦

0 0 1

0 0 0

0 0 0

As is easy to see, A3 = O, and all the higher natural powers of this matrix

are equal to zero.

Finally we obtain

⎡

⎤

1 1 1/2

⎢

⎥

exp(A) = ⎢0 1 1 ⎥ .

⎣

⎦

0 0 1

[**2.52**](#br88)[** ](#br88)Solution.

⎡

⎤

1 0 n

⎢

⎥

(1) By the mathematical induction method, it is easy to prove that An = ⎢0 1 0⎥

⎣

⎦

0 0 1

for all integer non-negative n.

⎡

⎤

∞ 1

∞ k

0

⎢

!

!⎥

k

k

⎢k=0

k=1

⎥

⎢

∞ 1

k!

⎥

According to the formula ([2.49](#br71)), we have eA = ⎢

0

0

0

⎥.

⎢

⎥

⎢

=0

⎥

k

⎣

∞ 1 ⎦

0

k!

k=0

The sums deﬁning the diagonal elements converge to Euler’s number e. The

∞ k

∞

1

∞ 1

sum (eA)13

\=

\=

\=

is also equal to e.

k!

(k − 1)!

k!

k=1

k=1

k=0

Thus, write the answer:

⎡

⎤

e 0 e

0 e 0

0 0 e

⎢

⎥

e

A = ⎢

⎥

.

⎣

⎦

(2) Having computed the arbitrary natural power of the matrix A, we obtain An =

⎡

⎤

1 0

n

⎢

⎥

⎢

⎥.

n 1 n(n + 1)/2

0 0

⎣

⎦

1

Calculation of the diagonal elements of the exponential and the element

(eA)13

is performed similarly to item (1) of this problem.





110

2 Matrix Algebra

The element positioned at the intersection of the second row and the third

∞ n(n + 1)

column is deﬁned by the sum (eA)23

\=

. Transform this sum to

2n!

n=1

the form

∞

∞

∞

∞

\+ 1

− 1 + 2

1 

1

2

(n

)

(n

)

\=

\=

\+

.

2(n − 1)!

2(n − 1)!

2

(n − 2)!

2(n − 1)!

n=1

n=1

n=2

n=1

3

Therefore, (eA)23

\=

e.

2

As a result we obtain

⎡

⎣

⎤

2 ⎦

e 0 e

⎢

⎥

3

⎢

⎥

eA = ⎢e e e⎥ .

0 0 e

[**2.53**](#br88)[** ](#br88)Solution.

(1) According to the formula ([2.53](#br72)), we have

1

ln A = (A − I) − (A − I)2 + · · · ,

2

or

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

2

1 0 1

0 0 1

0 0 1

0 0 1

⎢

⎥

⎢

⎥

1 ⎢

⎥

⎢

⎥

ln ⎢0 1 0⎥ = ⎢0 0 0⎥ − ⎢0 0 0⎥ + · · · = ⎢0 0 0⎥ .

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

2

0 0 1

0 0 0

0 0 0

0 0 0

(2) After computing the lower powers of the matrix (A−I) we can write the general

formula for (A − I)n, where n  1:

⎡

⎤

0 0

δn1

⎢

⎥

(A − I)

n = ⎢

0 δn1 + δ

⎥

,

⎣ n1

δ

n2⎦

0 0

0

where δij is the Kronecker symbol.





Answers and Solutions

111

This implies that

⎡

⎢

⎤

⎥

⎡

⎢

⎤

⎥

0 0 1

1

1 0 1

⎢

⎥

ln ⎢1 1 1⎥ = 1 0

.

⎢

⎥

⎣

⎦

⎣

2⎦

0 0 1

0 0 0

[**2.54**](#br88)[** ](#br88)Hint.

Use the formula ([2.49](#br71)) and apply the mathematical induction method.

[**2.56**](#br88)[** ](#br88)Answer:

A square matrix of size 3 × 3 after reducing it to the echelon form with the help

of the elementary transformations can take one of the following forms:

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

1 a b

0 1 c

0 0 1

1 a b

0 1 c

0 0 0

1 a b

0 0 1

0 0 0

1 a b

0 0 0

0 0 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

,

,

,

.

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

Here, by a, b and c are denoted the arbitrary real numbers.

[**2.57**](#br88)[** ](#br88)Answer:

(1) addition the j-th row to the i-th row for j > i;

(2) addition the j-th column to the i-th column for j < i.

[**2.58**](#br88)[** ](#br88)Solution.

(1) Perform the following elementary transformations: add to the second row the

ﬁrst one, subtract from the third row the doubled ﬁrst one, then add to the third

row the second row.

⎡

⎤

1 2 −4 3 −2

⎢

⎥

We will obtain the matrix in the echelon form: A → ⎢0 5 −10 1 2 ⎥, its

⎣

⎦

0 0

0 0 12

rank is equal to rk A = 3.

(2) Subtract from the second row half of the ﬁrst one, subtract from the fourth row

two ﬁrst rows, swap the second and the third rows, subtract from the fourth row

the second one, swap the third and the fourth rows and, ﬁnally, subtract from

the fourth row half of the third row.

⎡

⎤

⎥

2 −4 3 1 0

0 1 −1 3 1

0 0 −1 −9 4

⎢

⎥

⎢

⎥

⎢

⎥

We obtain A →

, therefore, rk A = 3.

⎢

⎢

⎥

⎣

⎦

0 0

0

0 0





112

2 Matrix Algebra

(3) Let us use the elementary transformation method. Subtract from the second row

the quadruplicated ﬁrst row, subtract from the third row the ﬁrst one, subtract

from the fourth row the doubled ﬁrst row. Then, subtract from the third row the

second one, multiplied by 5/9. Finally, subtract from the fourth row the second

one, divided by 3.

Then we obtain

⎡

⎤

1 2

1

3

⎢

⎥

⎢

⎥

0 −9 −9 −18

0 0

⎢

⎥

A = ⎢

⎥ ,

⎢

⎥

0

0

⎣

⎦

0 0

0

0

therefore, rk A = 2.

(4) Swap the ﬁrst and the second rows, add to the third row the triplicated ﬁrst

row, add to the ﬁfth row the doubled ﬁrst row. Then, add to the third row

the second one, multiplied by 11/2. Subtract from the fourth row the second

one, multiplied by 5/2. Add to the ﬁfth row the second one, multiplied by 5/2.

Finally, subtract from the ﬁfth row the third one, multiplied by 2/3.

⎡

⎤

−1 −4 −5

⎢

⎥

⎢

⎥

0

2

−4

⎢

⎥

⎢

⎥

After the said transformations we obtain A → ⎢ 0 0 −30⎥, therefore,

⎢

⎥

⎢

⎥

⎢ 0

0

0

0 ⎥

⎣

⎦

0

0

the rank of this matrix is equal to three.

(5) Perform the following elementary transformations: subtract from the second

row the ﬁrst row, multiplied by 1/3. Then, subtract from the third row the

ﬁrst one, multiplied by 1/3. And ﬁnally, subtract from the third row the

quadruplicated second row.

⎡

⎤

3 5

7

⎢

⎥

After that we obtain A → ⎢0 1 3 2 3⎥, the rank of such a matrix is equal

/

/

⎣

⎦

0 0

0

to two.

(6) The matrix is presented in the echelon form, and, as is easy to see, rk A = 3.

(7) Add to the second row the doubled ﬁrst row, subtract from the third row the

doubled ﬁrst row, add to the third row the second row.





Answers and Solutions

113

Then we obtain

⎡

⎤

1 −1 2 4 3

⎢

⎥

A → 0 −1 9 10 12

⎢

⎥

,

⎣

⎦

0 0 9 9 8

and the rank of the matrix A is equal to three.

(8) Subtract from the second row the doubled ﬁrst row, subtract from the third row

the ﬁrst one, multiplied by ﬁve. Then, subtract from the fourth row the ﬁrst

one, multiplied by seven. Subtract from the third row the doubled second one

and swap the third and the fourth rows. Finally, subtract from the third row the

doubled second row.

After the said transformations we obtain

⎡

⎤

1 3 5 −1

0 −7 13 6

0 0 0 −4

⎢

⎥

⎢

⎥

⎢

⎥

A → ⎢

⎥ ,

⎢

⎥

⎣

⎦

0 0

0 0

therefore, rk A = 3.

[**2.59**](#br89)[** ](#br89)Solution.

1

1

Consider the minor of the ﬁrst order M = β − γ . If β = γ , then the rank of the

matrix  is no less than one.




` `−

0 

β

γ

Then, consider the minor of the second order M1,2

\=


. If the

1,2


γ − α −γ 

condition γ = 0 is fulﬁlled, then rk   2.

Finally, compute the bordering minors of the third order:




− γ

0

γ

β



1,2,3

1,2,3


M

= γ − α −γ

0

= 0,




` `−

− 

α

β β

α




− γ 0 −β

β



1,2,3

1,2,4


M

= γ − α −γ α = 0.




` `−

0 

α

β β

Therefore, the maximum value that the rank of the matrix  can take is equal to

two.





114

2 Matrix Algebra

Note that with the help of the Kronecker symbol (see page [4](#br19)) the formula for the

rank of this matrix can be written in the form rk  = 2(1 − δ

[**2.60**](#br89)[** ](#br89)Solution.

α0 β0 γ 0

δ δ

).

(a) Use the bordering minor method (see page [64](#br78)):




1 

λ

1

1,2

1 2

,


M = 1 = 0,

M

\=

= 1 − λ.

1


1 1

Then, consider two cases.

⎡

⎤

⎡

⎤

1 1 0

1 1 0

⎢

⎥

(2)−(1) ⎢

⎥

(1) If λ = 1, then the matrix is equal to ⎢1 1 0⎥ → (2)↔(3) ⎢0 0 1⎥. It is clear

⎣

⎦

⎣

⎦

0 0 1

0 0 0

that its rank is equal to two.

(2) If λ = 1, then we compute the bordering minor of the third order (it is the

only one):





1 λ 0




1,2,3

1,2,3


M

= 1 1 0 = 1 − λ = 0.



0 0 1

Therefore, the rank of the matrix is equal to

2, if λ = 1,

3, if λ = 1.

(b) The lower minor M1 = 1 − λ.

1

Then, consider two cases.

⎡

⎤

0 0 0

⎢

⎥

(1) If λ = 1, then the matrix is equal to ⎢0 1 0⎥, and its rank, as is easy to see,

⎣

⎦

0 0 2

is equal to two.

(2) If λ = 1, then we continue to compute the bordering minors:




1 −

0

λ

1,2

1,2


M

\=

= (1 − λ)(2 − λ).



0

2 − λ





Answers and Solutions

115

⎡

⎤

−1 0 0

⎢

⎥

If λ = 2, we obtain the matrix ⎢ 0 0 0⎥, its rank is equal to two.

⎣

⎦

0 0 1

1,2,3

1,2,3

1,2,3

1,2,3

If λ = 2, then we need to compute the bordering minor M

(1 − λ)(2 − λ)(3 − λ).

: M

\=

⎡

⎤

−2 0 0

⎢

⎥

In the case when λ = 3, the matrix is equal to ⎢ 0 −1 0⎥, its rank is equal

⎣

⎦

0

0 0

to two. Otherwise, the rank is equal to three.

As a result, we form the answer:

2, if λ ∈ {1, 2, 3},

3, otherwise.

(c) Since M1 = 1 = 0, then the rank of the matrix is no less than one.

1

Then, consider the minors of the second order:




` `1

2

1,2

1,2


M

\=

= 4 − λ.


−1 2 − λ

This minor is not equal to zero at λ = 4. For this case, consider the bordering

minor of the third order:




1

2

−3




1,2,3

1,2,3

= −1 2 − λ 10 = λ2 − 4λ − 14.


M




−1

0

3 − 

λ

√

The determinant is equal to zero for λ = 2 ± 3 2. For such values of λ the

rank is equal to two; for other values the rank is equal to three.

Now consider the case λ = 4.

Then the non-zero minor of the second order:





2

−3

1,2

2,3


M

\=

= 14 = 0.


2 − λ 10

Then, the rank is no less than two. The third order minor is the only one, but

it is only equal to zero for λ = 2 ± 3 2, as is shown above. Then, in this case

√

the rank is equal to three.





116

2 Matrix Algebra

√

So, for λ = 2 ± 3 2 the rank of the matrix is equal to two, for other λ the

rank of the matrix is equal to three.

1

(d) There exists M = 1 = 0, therefore, the rank of the matrix is no less than one.

2

Then, consider the minors of the second order:




−

1

λ

1,2

1,2


M

\=

= λ(λ − 1).


` `0 1 − λ

This minor is not equal to zero at λ = 0 and for λ = 1. For this case, such

for the minor of the third order:




−λ

1

1

1




1,2,3

1,2,3


M

\=

0 1 − λ

= λ(λ − 1)(2 − λ).




` `0

0

2 − 

λ

λ(λ − 1)(2 − λ) = 0 for λ = 2 (since λ = 1 and λ = 0). In this case, the

rank is equal to three.

For λ = 2 the rank is equal to two.

Assume that now λ = 0:

⎡

⎤

0 1 1

0 1 1

0 0 2

⎢

⎥

⎢

⎥

,

⎣

⎦




1 1

2,3

2,3


M

\=

= 2 = 0.


0 2

Then, the rank is more than two.





0 1 1





` `= 0

0 1 1

.



0 0 2

Then, in this case the rank is equal to two.





Answers and Solutions

117

Now consider λ = 1:

⎡

⎤

−1 1 1

0 0 1

0 0 1

⎢

⎥

⎢

⎥

.

⎣

⎦




1 1

The rank is equal to two, because M1,2

\=


= 1 = 0, and the

2,3


0 1

determinant of the matrix is equal to zero.

Therefore, the rank is equal to two for λ ∈ {0, 1, 2}, and is equal to three in

other cases.

(e) The minor of the ﬁrst order is M1 = 1 = 0, therefore, the rank of the matrix

1

takes the value no less than one.

Let us ﬁnd the bordering minor of the second order:




` `1 −6 

1,2

1,2


M

\=

= −4 − λ.


−1 2 − λ

This minor is not equal to zero if λ = −4. Let us ﬁnd the minor of the third

order for such values of λ:




1

−6 −5




1,2,3

1,2,3


= λ2 + 8λ + 16.

M

= −1 2 − λ

5




−1

6

1 − 

λ

This expression may only be equal to zero for λ = −4. Therefore, in this

case the rank is equal to three.

Now consider the case when λ = −4.

⎡

⎤

1 −6 −5

−1 6

−1 6

⎢

⎥

⎢

⎥

5

.

⎣

⎦

5

The rank of the obtained matrix is equal to one.

As a result, the rank is equal to one for λ = −4, and is equal to three for

λ = −4.





118

2 Matrix Algebra

2

(f) There exists M = 1 = 0, therefore, the rank is no less than one.

1

Let us ﬁnd the minors of the second order.




1 −

2

λ

1,2

1,2


M

\=

= λ(λ − 3).



1

2 − λ

It is not equal to zero if λ = 0 and λ = 3. Find for such values of the

parameter λ the bordering minors of the third order.




1 − λ

2

2 − λ

0

0

0




1,2,3

1,2,3


M

\=

1

= λ(λ − 3)(3 − λ).





0

3 − 

λ

The third order minor is non-zero for all considered in this case λ. Let us ﬁnd

the minor of the fourth order (it is the only one):




1 − λ

1

0

0

2

2 − λ

0

0

0

0

0

0








= λ(λ − 3)(3 − λ)(4 − λ).




3 − λ

0





0

4 − 

λ

It is equal to zero only for λ = 4. For this case, the rank is equal to three. For

λ = 4 the rank is equal to four.

Then, consider the value λ = 0:




3 0

3,4

3,4


M

\=

= 12 = 0,


0 4




3 0 0




2,3,4

2,3,4


M

= 0 3 0 = 24 = 0.




0 0 4

For λ = 0 the determinant of the initial matrix is equal to zero. Then, the

rank is equal to three.





Answers and Solutions

119

For λ = 3:

⎡

⎤

−2 2 0 0

1 −1 0 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ .

⎢

⎥

0

0 0 0

⎣

⎦

0

0 0 1

There is no minor of the third order that is not equal to zero. Therefore, the

rank is equal to two.

Finally we obtain the rank is equal to two for λ = 3, is equal to three for

λ ∈ {0, 4}, is equal to four in other cases.

2

(g) There exists M = 0, therefore, the rank is no less than one.

1

Let us ﬁnd the minors of the second order:




1 −

2

λ

1,2

1,2


= −(λ2 + 1) = 0.

M

\=



1

1 + λ

This minor is always other than zero. Consider the bordering minors of the

third order:




1 − λ

2

1 + λ

0

0

0





` `= 2 −

− 2 − 1 = 0 only for = 2 but

1

(

λ)( λ

)

λ

,





0

2 − 

λ




1 − λ

2

1 + λ

0

0





` `= 2 +

− 2 − 1 = 0 only for = −2

1

0

(

λ)( λ

)

λ

.





0

2 + 

λ

This is because the minors of the third order are not simultaneously equal to

zero.

Calculate the determinant of the initial matrix (in other words, ﬁnd the minor

of the fourth order):




1 − λ

1

0

0

2

1 + λ

0

0

0

0

0

0








= (2 + λ)(2 − λ)(−λ2 − 1).




2 − λ

0





0

2 + 

λ





120

2 Matrix Algebra

For λ = ± 2:

(2 + λ)(2 − λ)(−λ

2 − 1 = 0, therefore, the rank is equal to three.

)

For other λ the rank is equal to four.

So, the rank is equal to three for λ = ± 2, and equal to four for λ = ± 2.

2

(h) There exists M = 0, therefore, the rank is no less than one.

1

Let us ﬁnd the minors of the second order:




1 + 2

λ

1,2

1,2


M

\=

= λ − 1 = 0 for λ = 1.



1

1

For this case, ﬁnd the minors of the third order:




1 + λ 2 4




1,2,3

1,2,4


1 0 = −(λ − 1) = 0.

M

\=

1





0

0 −1

Then, the rank is greater than or equal to three. Calculate the determinant of

the initial matrix:




1 + λ 2

0

0

4

0






1

0

1

1


= λ2 − λ − 12.




0 2 + λ −1





0

2

1 

The determinant is equal to zero for λ = 4 or −3. Hence, for such values

of the parameter λ the rank is equal to three. In other cases the rank is equal to

four.

Now consider the case when λ = 1. Let us ﬁnd the minor of the second

order:




1 0

2,3

2,3


M

\=

= 3 = 0.


0 3

Calculate the minor of the third order:





2 0 4




1,2,3

1,2,4


M

= 1 0 0 = 12 = 0.



0 3 −1





Answers and Solutions

121

Then, the rank of the matrix is no less than three. Now ﬁnd the determinant

of the initial matrix.




2 2 0 4

1 1 0 0

0 0 3 −1








= −12 = 0.








1 0 2 1 

This implies that in this case the rank is equal to four.

So, the rank is equal to three for λ ∈ {−3, 4}, and is equal to four in other

cases.

(i) The size of the matrix is equal to (n + 1) × (n + 1). As is easy to see, for

λ ∈ {0, 1, . . . , n} the determinant of the matrix takes the value equal to zero.

We should also note that in this case there exists a minor of the order n, other

than zero. For example, for λ = 0:

⎡

⎤

1 − λ

1

1 . . .

1

1

1

1

⎢

⎥

⎢

⎥

0

2 − λ 1 . . .

⎢

⎥

⎢

⎥

⎢

⎥

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

.

⎢

⎥

⎢

⎥

⎢

0

0

0

0

0

− 1 −

0

1

⎥

. . . (n

)

λ

⎣

⎦

0 . . .

n − λ

As is known, determinant of the upper triangular matrix is equal to the

product of the diagonal terms of the matrix. Since the condition λ = 0 is

fulﬁlled, then this product is not equal to zero. Therefore, the rank of the initial

matrix in this case is equal to n. Yet, if the condition λ ∈ {0, 1, . . ., n} is not

fulﬁlled, then the rank of the initial matrix takes the value equal to n + 1.

We obtain the ﬁnal answer: the rank of the matrix is equal to n for λ ∈ {0, 1, . . . , n},

and is equal to n + 1 for other values of λ.





**Chapter 3**

**Systems of Linear Equations**

The system of m linear equations with n unknowns is written as

⎧

⎪

\+

\+ · · · +

\=

⎪ a x

a x

12

a x

1n

1

b ,

⎪

11

1

2

n

⎪

⎪

⎨

a21x1 + a22x2 + · · · + a2 x = b2,

n

n

(3.1)

⎪

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

a

m

1x1 + a 2x2 + · · · + amnx = b .

m

n

m

Here, by x , x , . . . , x are denoted unknown numbers, a and bi are prescribed

1

2

n

ij

numbers, also referred to as **coefﬁcients** of the system of equations ([3.1](#br136)). Variables

bi are called **known terms** or right-hand sides of equations.

**Solution of the system of equations** is such a collection of n numbers, which

when x , x , . . . , x are substituted into the system in place of the unknown, turns

1

2

n

all the equations into identities. The solution is written as a vector [x , x , . . . , x ]T .

1

2

n

If b = 0 for all i = 1, 2, . . . , m, then the system of equations is called

i

**homogeneous**. If at least one of the known terms is b = 0, then the system of

i

equations is called **non-homogeneous**.

In case when m = n, the system of equations is called **square**, and when m = n,

the system is called **rectangular**.

A system of linear equations is called [**consist](#br422)**ent**, if it has at least one solution,

and **inconsistent**, if there are no solutions [[65](#br422)[\].](#br422)

If a consistent system has the only solution, it is called **determined**. If the

consistent system has at least two different solutions, it is called **undetermined**.

© Springer Nature Switzerland AG 2021

123

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_3>





124

3

Systems of Linear Equations

A matrix

⎡

⎤

a11 a12 . . . a1n

⎢

⎥

⎢

⎥

⎢a21 a22 . . . a2 ⎥

n

A = ⎢

(3.2)

⎥ ,

⎢

⎥

. . . . . . . . . . . . . .

⎣

⎦

a

m m mn

1 a 2 . . . a

consisting of coefﬁcients of the unknown aij is called a **system matrix**.

A matrix

⎡

⎤

a11 a12 . . . a1n | b1

⎢

⎥

⎢

⎥

| b

⎢a21 a22 . . . a2

2 ⎥

n

B = ⎢

(3.3)

⎥ ,

⎢

⎥

. . . . . . . . . . . . . . . . | . . .

⎣

⎦

| bm

a

1 a 2 . . . a

m

m

mn

into which a column of the constant terms bj is added is called an **augmented**

**system matrix**.

If the unknown and constant terms are written in the form of a column (of

matrices of sizes n × 1 and m × 1, respectively):

⎡

⎤

⎡

⎤

x1

x2

b1

b2

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

X = ⎢ ⎥ , B = ⎢ ⎥ ,

(3.4)

.

.

⎢ . ⎥

⎢ . ⎥

⎣ . ⎦

⎣ . ⎦

x

b

n

m

then the system of equations ([3.1](#br136)) can be presented in an abridged **matrix form**:

A · X = B.

(3.5)

**3.1 Cramer’s Rule**

Consider a square system of n equations with n unknowns:

⎧

⎪

\+

\+ · · · +

\=

⎪ a x

a x

12

a x

1n

1

b ,

⎪

11

1

2

n

⎪

⎪

⎨

a21x1 + a22x2 + · · · + a2 x = b2,

n

n

(3.6)

⎪

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

a 1x1 + a 2x2 + · · · + a x = b .

n

n

nn

n

n





3.1 Cramer’s Rule

125

**Theorem 3.1 (Cramer’[s**](#br138)[**1](#br138)[ ](#br138)Rule)** If the determinant of the matrix A of the sys-

tem ([3.6](#br137)) is other than zero, then the system ([3.6](#br137)) is **determined**, i.e. it has the **unique**

**solution**. This solution can be computed by the formula

i

xi =

, i = 1, 2, . . ., n.

(3.7)

Here, i is the determinant of the matrix obtained from the initial matrix A by

replacement of the i-th column with a column of constant terms:




` `a11 . . . a1 −1 b1 a1 +1 . . . a1 

i

i

n




a21 . . . a2 −1 b2 a2 +1 . . . a2

i

i

n 

` `= 

(3.8)

` `.

i

.

.

.

.

.

.

.

` `.

.

.

.

.

.

. 

` `.

.

.

.

.

.

. 




a 1 . . . a −1 bn an i+1 . . . a

n

n i

nn

If  [=](#br137)[ ](#br137)0 and at least one of the determinants  is other than zero, then the

i

system ([3.6](#br137)) has no solutions (i.e. it is inconsistent).

If  = 0, but also  = 0, then the system ([3.6](#br137)) has inﬁnitely many solutions

i

(i.e. it is consistent but undetermined) or is inconsistent.

Example 3.1 Solve the system:

⎧

⎨

5x − 6y = −8,

5x + 6y = 28.

(3.9)

⎩

For the given system we have












5 −6

−8 −6

5 −8

` `=

` `= 60

, x

\= 

` `= 120

, y

\= 

` `= 180

.

(3.10)






5 6 

` `28 6 

5 28 

Thus, according to Cramer’s rule

x

120

60

y

180

60

x =

\=

= 2, y =

\=

= 3.

(3.11)


1Gabriel Cramer (1704–1752) was a Genevan mathematician.





126

3

Systems of Linear Equations

Example 3.2 Solve the system of linear equations:

⎧

⎪2 − + 3 = 8

⎪ x

y

z

,

⎨

x + y − 2z = 5,

3x − 2y + z = 7.

(3.12)

⎪

⎪

⎩

**Solution** Compute the determinants required to apply Cramer’s rule:










2 −1 3

8 −1 3








` `= 1 1 −2

` `= −14

, x

\= 

5 1 −2

` `= −56

,

(3.13)

(3.14)






` `3 −2 1 

` `7 −2 1 








2 8 3

2 −1 8

1 1 5








` `= 1 5 −2

` `= −42

, z

\= 

` `= −14

.

y








` `3 7 1 

3 −2 7

Therefore

x

y

z

x =

= 4, y =

= 3, z =

= 1.

(3.15)


**3.2 Inverse Matrix Method**

Consider the system of equations ([3.6](#br137)). Write this system in the form A · X = B in

accordance with ([3.5](#br137)).

Let the matrix A have the inverse one A−1. Multiply both sides of the equality

A · X = B by A−1 on the left:

A−1 · A · X = A−1 · B.

(3.16)

Transform the obtained matrix equation. Since the identities A−1 · A ≡ I and

I · X ≡ X are valid, the solution of the system X can be written in the form

X = A−1 · B.

(3.17)

Therefore, if we ﬁnd the inverse matrix A−1, then the solution of the system can

be obtained as the product of the matrices A−1 and B.





3.2 Inverse Matrix Method

127

Example 3.3 Solve the system of equations

⎧

⎪−2 + 2 − 3 = −10

⎪

x

y

z

,

⎨

2x − y + 2z =

3x − y + 3z = 10

7,

(3.18)

⎪

⎪

⎩

by the inverse matrix method.

**Solution** The matrix of the analysed system of equations A has the form:

⎡

⎤

−2 2 −3

2 −1 2

3 −1 3

⎢

⎥

⎢

⎥

(3.19)

.

⎣

⎦

We ﬁnd the inverse matrix using a cofactor matrix. The determinant of the matrix

A is equal to












−1 2

2 2

2 −1

det A = −2 

` `− 2   − 3 







−1 3

3 3

3 −1

= (−2)(−3 + 2) − 2(6 − 6) − 3(−2 + 3) = −1.

(3.20)

Calculate the cofactors:








−1 2

2 2

1+1 

1+2 

A11 = (−1)

= −1, A12 = (−1)

= 0,

(3.21)

(3.22)

(3.23)

(3.24)

(3.25)




−1 3

3 3








2 −1

` `2 −3

A13 = (−1)1+3 

= 1, A21 = (−1)

2+1 

= −3,




3 −1

−1 3 








−2 −3

−2 2 

2+2 

2+3 

A22 = (−1)

= 3, A23 = (−1)

= 4,




` `3 3 

` `3 −1








` `2 −3

−2 −3

A31 = (−1)3+1 

= 1, A32 = (−1)

3+2 

= −2,




−1 2 

` `2 2 




−2 2 

A33 = (−1)3+3 

= −2.


` `2 −1





128

3

Systems of Linear Equations

Write the matrix formed by the cofactors:

⎡

⎤

−1 0

−3 3

1

4

⎢

⎥

⎢

⎥

(3.26)

.

⎣

⎦

1 −2 −2

As a result, the desired inverse matrix will have the form:

⎡

⎤

⎡

⎤

−1 −3 1

1

3 −1

1

⎢

⎥

⎢

⎥

A−1

\=

⎢

⎥

\=

⎢

⎥

.

(3.27)

0

3 −2

4 −2

0 −3 2

−1 −4 2

⎣

⎦

⎣

⎦

(−1)

1

Then, the solution of the system will be found using the matrix multiplication

operation:

⎡ ⎤

⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤

x

1

3 −1

−10

−10 + 21 − 10

0 − 21 + 20

10 − 28 + 20

1

−1

2

⎢ ⎥

⎢

⎣

⎥ ⎢

⎥

⎢

⎥

⎢

⎥

⎢ ⎥ = ⎢

⎥ ⎢

⎥ = ⎢

⎥ = ⎢

⎥

(3.28)

y

0 −3 2

7

.

⎣ ⎦

⎦ ⎣

⎦

⎣

⎦

⎣

⎦

z

−1 −4 2

10

**3.3 Gaussian Elimination**

The use of the notion of matrix rank allows obtaining the criterion of consistency of

the system of linear equations.

Consider the system:

⎧

⎪

\+

\+ · · · +

\=

⎪ a x

a x

12

a x

1n

1

b ,

⎪

11

1

2

n

⎪

⎪

⎨

a21x1 + a22x2 + · · · + a2 x = b2,

n

n

(3.29)

⎪

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

a

m

1x1 + a 2x2 + · · · + amnx = b .

m

n

m





3.3 Gaussian Elimination

129

The augmented matrix of the system of size m × (n + 1) has the form:

⎡

⎤

a11 a12 . . . a1n | b1

⎢

⎥

⎢

⎥

| b

⎢a21 a22 . . . a2

2 ⎥

n

B = ⎢

(3.30)

⎥ .

⎢

⎥

. . . . . . . . . . . . . . . . | . . .

⎣

⎦

m

1 a 2 . . . a

m

mn

| bm

a

The consistenc[y](#br142)[ ](#br142)criterion for the system of linear algebraic equat[ions](#br142)[ ](#br142)is the

[Kroneck](#br422)er–Capelli[2](#br142)[ ](#br142)theorem (also referred to as the theorem of Rouché[3](#br142)–Capelli)

[[64](#br422)[\].](#br422)

**Theorem 3.2 (Kronecker–Capelli Theorem)** A system of linear algebraic equa-

tions ([3.29](#br141)) is consistent if and only if the rank of the basic matrix A equals to the

rank of the augmented one, i.e. rk A = rk B = r.

If r = n, then we obtain a square matrix with a non-zero determinant. Its solution

exists and it is unique.

If r < n and the system is consistent, then there exists an inﬁnite set of solutions.

If rk B > rk A, then the system is inconsistent.

In what follows, by **zero equations** we will understand the equations of the form

0 · x + 0 · x + · · · + 0 · x = 0.

1

2

n

**Elementary transformations** of the system of linear equations are:

\1. interchange (swap) of any two equations;

\2. multiplying the equation by any non-zero number;

\3. adding to the equation another one multiplied by an arbitrary number;

\4. dropping the zero equations.

Gaussian[4](#br142)[ ](#br142)method or **Gaussian elimination** consists in transformation of the

augmented matrix B with the help of the elementary transformations to the echelon

form. Such transformations are aimed at obtaining a system of the form:

⎧

⎪

·

x1 b12 x2

\+

·

\+ · · · +

·

\+ · · · +

·

\=

⎪b

b1r xr

1

b1n xn p ,

⎪

11

⎪

⎪

⎨

b22 · x2 + · · · + b2 · x + · · · + b2 · x = p2,

r

r

n

n

(3.31)

⎪

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

b

· x + · · · + b · x = p .

rr

r

rn

n

r

Note that for bringing the system of equations to the said form we may need to

change the numbering of the variables.

2Alfredo Capelli (1855–1910), Italian mathematician.

3Eugène Rouché (1832–1910), French mathematician.

4Johann Carl Friedrich Gauß (1777–1855), prominent German mathematician and astronomer.





130

3 Systems of Linear Equations

The system ([3.31](#br142)) may contain less equations than the initial one due to dropping

of the zero equations of the form:

0 · x + 0 · x + · · · + 0 · x = 0.

(3.32)

1

2

n

If the transformations result in the equation

0 · x + 0 · x + · · · + 0 · x = d = 0,

(3.33)

1

2

n

then the system is inconsistent.

It is obvious that the minor M

are free unknowns, to which we can assign arbitrary values:

1,2,...,r

1,2,...,r

is a basic minor, assuming that xr+1, . . . , xn

x +1 = C1, . . . , x = C − .

(3.34)

r

n

n r

Rearrange these variables to the right side; then the obtained system necessarily

has a solution relative to the unknowns x , x , . . . , x .

1

2

r

From the last equation we ﬁnd xr, from the last but one we ﬁnd xr−1, etc.

Note Gaussian method is sometimes referred to as **method of successive elimina-**

**tion of unknowns**.

Example 3.4 Solve the system of equations by Gaussian method:

⎧

⎪

− 2

\+

= −3

⎪ x

x2

x4

,

⎪

1

⎪

⎪

⎨

3x − x − 2x

\=

1,

1

2

3

(3.35)

⎪

⎪ 2x + x − 2x − x = 4,

⎪

1

2

3

4

⎪

⎪

⎩

x1 + 3x2 − 2x3 − 2x4 = 7.

**Solution** Write the augmented matrix:

⎡

⎤

1 −2 0 1 | −3

⎢

⎥

⎢

⎥

3 −1 −2 0 | 1

2 1 −2 −1 | 4

1 3 −2 −2 | 7

⎢

⎥

(3.36)

⎢

⎥ .

⎢

⎥

⎣

⎦





3.3 Gaussian Elimination

131

Bring the obtained matrix to a triangular form. For this, subtract from the second

row the triplicated ﬁrst row, from the third row—the doubled ﬁrst one, and from the

fourth row—the ﬁrst one:

⎡

⎤

1 −2 0 1 | −3

0 5 −2 −3 | 10

0 5 −2 −3 | 10

0 5 −2 −3 | 10

⎢

⎥

⎢

⎥

⎢

⎥

(3.37)

⎢

⎥ .

⎢

⎥

⎣

⎦

In the next step, subtract from the third and the fourth rows the second one. The

ﬁrst and the second rows remain unchanged:

⎡

⎤

1 −2 0 1 | −3

0 5 −2 −3 | 10

⎢

⎥

⎢

⎥

⎢

⎥

(3.38)

⎢

⎥ .

⎢

⎥

0 0

0

0 | 0

0 | 0

⎣

⎦

0 0

0

It is clear that the ranks of the basic and the augmented matrices are equal to two.

The system is consistent and undetermined. As free variables, take x and x . Let

1

3

x1 = C1, and x3 = C2. Then we have

⎧

⎨

−2 · x + x = −3 − C1,

2

4

(3.39)

⎩

5 · x − 3 · x = 10 + 2 · C .

2

4

2

We are solving this system relative to the variables x and x :

2

4

⎧

⎨

x2 = −1 + 3 · C1 − 2 · C2,

x4 = −5 + 5 · C1 − 4 · C2.

(3.40)

⎩

We write the ﬁnal answer in the form:

⎡

⎤

⎡

⎤

⎡

⎤

⎡ ⎤

⎡

⎤

x1

C1

0

1

0

⎢

⎥

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

−1 + 3C1 − 2C

−1

0

3

−2

1

⎢x2⎥

⎢

2⎥

⎢

⎥

⎢ ⎥

⎢

⎥

X = ⎢ ⎥ = ⎢

⎥ = ⎢ ⎥ + C1 ⎢ ⎥ + C2 ⎢ ⎥ .

(3.41)

⎢

⎥

⎢

⎥

⎢

−5

⎥

⎢ ⎥

⎢

⎥

−4

x3

C2

0

⎣

⎦

⎣

⎦

⎣

⎦

⎣ ⎦

⎣

⎦

x4

−5 + 5C1 − 4C2

5






132

3 Systems of Linear Equations

Example 3.5 Solve the matrix equation relative to the unknown matrix Y:

⎡

⎤

⎡

⎤

⎡

⎤

1 −1

−1 2

1 3

1 3

−2 −6

⎣

⎦

⎣

⎦ = ⎣

⎦

(3.42)

Y

.

3

9

⎡

⎤

1 3

Note the degeneracy of one of the multipliers, namely the matrix ⎣ ⎦.

1 3

⎡

⎤

1 3

**Solution** Note that the degeneracy of the matrix ⎣ ⎦ does not allow us to use the

1 3

equation solving method with the help of the inverse matrix. In this case, reduce the

problem to the system of linear equations.

Denote the elements of the matrix Y by y , y , y and y :

1

2

3

4

⎡

⎤

y1 y2

y3 y4

Y =

⎣

⎦

.

(3.43)

Successively expand the product of the matrices:

⎡

⎤ ⎡

⎤ ⎡

⎤

⎡

⎤

⎡

⎤ ⎡

⎦ ⎣

⎤

1 −1

−1 2

y1 y2

y3 y4

1 3

−2 −6

y1 − y3

1

y2 − y4

2

1 3

⎣

⎦ ⎣

⎦ ⎣ ⎦ = ⎣

⎦ = ⎣

⎦

1 3

3

9

−y + 2y −y + 2y

1 3

3

4

⎡

⎤

y1 + y2 − y3 − y4

3y1 + 3y2 − 3y3 − 3y4

= ⎣

⎦ .

(3.44)

−y − y + 2y + 2y −3y − 3y + 6y + 6y

1

2

3

4

1

2

3

4

⎡

⎤

−2 −6

The obtained matrix is equal to ⎣

⎦.

3

9

Equating the respective elements of the matrices, we obtain a non-homogeneous

system of linear equations relative to the unknowns y , y , y and y :

1

2

3

4

⎧

⎪

\+

−

−

= −2

⎪

y1 y2 y3 y4

,

⎪

⎪

⎪

⎨

3y + 3y − 3y − 3y = −6,

1

2

3

4

(3.45)

⎪

⎪

−y − y + 2y + 2y = 3,

⎪

1

2

3

4

⎪

⎪

⎩

−3y − 3y + 6y + 6y = 9.

1

2

3

4





3.3 Gaussian Elimination

133

Write the augmented matrix of this system:

⎡

⎤

1

3

1 −1 −1 | −2

⎢

⎥

⎢

⎥

3 −3 −3 | −6

⎢

⎥

(3.46)

⎢

⎥ .

⎢

⎥

−1 −1 2 2 | 3

−3 −3 6 6 | 9

⎣

⎦

Subtract from the second row the ﬁrst row, multiplied by 3; then, subtract from

the fourth row the third row, multiplied by 3:

⎡

⎤

1

0

1 −1 −1 | −2

⎢

⎥

⎢

⎥

0

0

0 | 0

⎢

⎥

(3.47)

⎢

⎥ .

⎢

⎥

−1 −1 2 2 | 3

⎣

⎦

0

0

0

0 | 0

Then, add to the third row the ﬁrst row. The zero rows do not inﬂuence the

solution, this is why we obtain the following equivalent matrix:

⎡

⎣

⎤

⎦

1 1 −1 −1 | −2

0 0 1 1 | 1

.

(3.48)

(3.49)

It corresponds to the system of equations with four unknowns

⎧

⎨

y1 + y2 − y3 − y4 = −2,

y3 + y4 = 1.

.

⎩

The ranks of the basic and augmented matrices are equal to two. Therefore, we

conclude that the system ([3.49](#br146)) is consistent and undetermined.

As the independent variables, select, for example y and y :

2

4

y2 = C1, y4 = C2, where C1, C2 ∈ R.

(3.50)

Having substituted ([3.50](#br146)) into the system ([3.49](#br146)), we obtain

⎧

⎨

y1 + C1 − y3 − C2 = −2,

y3 + C2 = 1,

(3.51)

⎩





134

3

Systems of Linear Equations

or

⎧

⎨

y1 = −1 − C1,

y3 = 1 − C2.

(3.52)

⎩

Write the coefﬁcients y –y in the form of a column:

1

4

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

y1

−1

−1

0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0

1

0

−1

1

⎢y2⎥

⎢

⎥

⎢

⎥

⎢

⎥

\=

\+ C

\+ C

.

(3.53)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

2

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

y3

y4

1

0

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

0

0

As a result, the matrix Y is equal to

⎡

⎤

⎦

−1 − C1 C1

1 − C2 C2

Y =

⎣

,

(3.54)

where C , C are arbitrary real numbers.

1

2

Thus, the matrix equation [(](#br145)[3.42](#br145)) has the inﬁnite set of solutions, depending on

two real parameters.

Check

By direct substitution of the obtain matrix into ([3.42](#br145)) it is easy to check that Y is

determined correctly:

⎡

⎣

⎤ ⎡

⎦ ⎣

⎤ ⎡

⎤

1 −1

−1 − C1 C1

1 − C2 C2

1 3

1 3

⎦ ⎣

⎦

−1 2

⎡

⎤ ⎡

⎤

⎡

⎤

−2 − C1 + C2 C1 − C2

3 + C − 2C −C + 2C

1 3

−2 −6

= ⎣

⎦ ⎣ ⎦ = ⎣

⎦ .

1 3

3

9

1

2

1

2

Assume that A and B are arbitrary matrices with sizes m × n and n × p,

respectively. Estimate of the rank of the product of the matrices A and B is provided

by the following theorem.

**Theorem 3.3** The rank of the matrix product satisﬁes the inequality

rk AB  min(rk A, rk B).

(3.55)





3.3 Gaussian Elimination

135

In other words, the rank cannot increase when the matrices are multiplied [\[](#br422)[63](#br422)[,](#br422)

[64](#br422)[\].](#br422)

There exist many various methods of solving system of linear equations.

Gaussian method is one of the most frequently used.

Consider realization in Python of Gaussian method of solving system of linear

equations (Listing 3.1).

For deﬁniteness, we will form the solutions for the systems where the number

of equations and unknowns coincides, but the provided algorithm can easily be

transformed for the systems with an arbitrary relation between equations and

unknowns.

§

Listing 3.1¤

1 import math

2

3

4 def gaussian\_elimination(A, B):

5

6

m = len(A)

n = len(A[0])

7

8

if len(B) != m:

9

raise ValueError

10

11

12

13

14

15

16

17

18

19

20

21

22

23

24

25

26

27

28

29

30

31

32

C = [[A[i][j] if j != n else B[i] \

for j in range(n+1)] for i in range(m)]

\# Forward elimination

for r in range(min(n, m)):

max\_row\_pos = r

\# Pivoting strategy

for i in range(r + 1, m):

if abs(C[i][r]) > \

abs(C[max\_row\_pos][r]):

max\_row\_pos = i

C[r], C[max\_row\_pos] = \

C[max\_row\_pos], C[r]

if math.isclose(C[r][r], 0):

continue

for i in range(r + 1, m):

factor = C[i][r] / C[r][r]





136

3 Systems of Linear Equations

33

34

35

36

37

38

39

40

41

42

43

44

45

46

47

48

49

50

51

52

53

54

55

56

57

58

59

for j in range(r, n + 1):

C[i][j] -= factor \* C[r][j]

\# Back substitution

answer = [0] \* n

for i in range(min(n - 1, m - 1), -1, -1):

s = 0.0

for j in range(i + 1, n):

s += C[i][j] \* answer[j]

if not math.isclose(C[i][i], 0):

answer[i] = (C[i][n] - s) / C[i][i]

elif not math.isclose(C[i][n] - s, 0):

return None

for i in range(n, m):

s = 0.0

for j in range(n):

s += C[i][j] \* answer[j]

if not math.isclose(C[i][n] - s, 0):

return None

¦

¥

return answer

Two parameters arrive at the input of the given function: the coefﬁcient matrix

with the unknowns in the system of equations A and the right side matrix B.

The realization of the function consists of three main steps. In the ﬁrst step, the

matrix C is constructed, which is obtained by attributing the matrix B to the initial

matrix A on the right.

Then, the so-called forward pass is performed with the purpose of bringing the

matrix to the echelon form (that is to the form when each successive row, viewed

from left to right, contains more zeroes than the previous one). This procedure is

performed by applying to the matrix C of a series of elementary transformations

by the following algorithm: successively, starting from the ﬁrst one, all columns

are scanned. Among the elements of the current column, the one with the greatest

module is found, referred to as the **basic** or **pivot**. Then, from each row, a row

is subtracted that contains the pivot and is multiplied by the coefﬁcient equal to

the relation of the row element in the considered column to the pivot. Thus, all

the elements in the column, except the pivot, become equal to zero. The process

is performed until the matrix has a row left that contains only two variables: one

coefﬁcient of the unknown and one value in the right side.





3.4 Fundamental System of Solutions of Homogeneous Systems

137

In the third step, the “backward pass” is performed. The values of all unknowns

are consequently expressed in terms of the already found variables. So, the unique

solution is obtained or it is determined that there are no solutions or the the set of

solutions is inﬁnite. The backward pass starts from the row containing the minimum

number of non-zero coefﬁcients, and continues until all the unknowns are expressed

in terms of the already known ones, or until it is established that there is no unique

solution.

The asymptotic complexity of Gaussian elimination, due to triple loop nesting

by the variables r, i, j, is equal to O(n3), where n is the number of equations in

the system.

Let us give an example (see Listing 3.2) of using the function

gaussian\_elimination(A, B) for solving the system of equations whose

matrix of size 100 × 100 has unities on the secondary diagonal and other elements

equal to zero. The column B is equal to [1, 2, 3, 4, . . ., 100].

§

¤

Listing 3.2

1 size = 100

2

3 A = [[0 for j in range(size)] \

4

for i in range(size)]

5 B = [0 for i in range(size)]

6

7 for i in range(size):

8

9

for j in range(size):

A[i][j] = 1 if j == size - i - 1 else 0

10

11 for i in range(size):

12

13

B[i] = float(i)

¦

¥

14 print(gaussian\_elimination(A, B))

**3.4 Fundamental System of Solutions of Homogeneous**

**Systems**

Consider a homogeneous system of equations that has the form

⎧

⎪

\+

\+ · · · +

= 0

⎪ a x

a x

12

1n

a x

n

,

⎪

11

1

2

⎪

⎨

a21x1 + a22x2 + · · · + a2 x = 0,

n

n

(3.56)

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

a

m

1x1 + a 2x2 + · · · + amnx = 0,

m

n

where m is the number of equations, n is the number of unknowns.

This system can be written in a matrix form:





138

3

Systems of Linear Equations

A · X = 0,

(3.57)

where A is the system matrix, and by X is denoted the column formed by the

variables:

⎡

⎤

x1

x2

⎢

⎥

⎢

⎥

⎢

⎥

X = ⎢ ⎥ .

(3.58)

.

⎢ . ⎥

⎣ . ⎦

x

n

This system necessarily has the solution X = [0, 0, . . ., 0]T , which is called

**trivial**.

Our purpose is to ﬁnd all non-trivial solutions, if any.

**Theorem 3.4** Let the matrix A of a homogeneous system of equations have the size

m × n and the rank r. If r = n, then the system has only a trivial solution. If

r < n, then there exist exactly n − r linearly independent solutions, referred to as

**fundamental system of solutions**.

Suppose that we have found the basic minor and it is located in the upper left

corner (otherwise, the order of variables and equations may be changed). Let us

keep only those equations whose coefﬁcients are included into the basic minor, that

is from the ﬁrst to the r-th. The unknowns from number r + 1 to number n are

referred to as **free** and rearranged to the right side of the equations:

⎧

⎪

\+ · · · +

= −

a1 +1x +1

− · · · −

⎪a11x1

a1rxr

a1 x ,

n n

⎨

r

r

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

(3.59)

⎪

⎪

⎩

a 1x1 + · · · + a x = −a +1x +1 − · · · − a x .

r

rr

r

rr

r

rn n

Let us introduce for consideration a square matrix

⎡

⎣

⎤

⎦

a11 . . . a1r

⎢

⎥

⎢ .

. ⎥

.

C = ⎢ .

.

. ⎥ ,

(3.60)

.

. .

a 1 . . . a

r

rr

and, according to the property of a basic minor, the following inequality det C = 0

is valid.





3.4 Fundamental System of Solutions of Homogeneous Systems

139

Denote

⎡

⎤

⎡

⎤

x1

x2

xr+1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

x +2

⎢

⎢

⎥

⎥

⎢ r

⎥

Y = ⎢ ⎥ ∈ R ,

r

Z

\=

∈ Rn−r .

(3.61)

⎢

⎥

.

.

⎢

⎥

.

.

⎣ . ⎦

⎣ . ⎦

x

x

r

n

Then, select n − r linearly independent vectors Z , Z , . . . , Z . Usually,

1

2

n−r

collections are taken that form the so-called **canonical basis** in Rn−r :

⎡ ⎤

⎡ ⎤

⎡ ⎤

1

0

0

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

0

1

0

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

Z1 =

⎢0⎥

,

Z2

= ⎢0⎥

,

. . . , Zn−r

= ⎢0⎥

.

(3.62)

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

.

.

.

⎢.⎥

⎢.⎥

⎢.⎥

.

.

.

⎣ ⎦

⎣ ⎦

⎣ ⎦

0

0

1

Let us call F the vector in the right side of the equation for the given Z , ...,

1

1

F − —for Z − .

n

r

n r

In this case, we have the systems of equations in a matrix form:

⎧

⎪

·

\=

⎪

C Y1

F1,

⎨

. . . . . . . . . . . . . . . .

(3.63)

⎪

⎪

⎩

C · Y − = F − .

n

r

n r

According to Cramer’s rule, the solutions Y , Y , . . . ,

Y

n−r

are uniquely

1

2

determined. Then the full solution of the system will consist of the vectors:

⎛

⎞

⎛

⎞

Y1

Y −

Zn−r

X1 =

⎝

⎠

, . . . , Xn−r

= ⎝

n

r ⎠

,

(3.64)

Z1

that are linearly independent, since Z1, . . . , Z

The set of the solutions X , X , . . . , X

are linearly independent.

represents the **fundamental system**

n−r

1

2

n−r

**of solutions (FSS)**.

If the free unknown is the only one in the system, then we assign a value to it

equal to one. If there are no free unknowns, i.e. r = n, then such a system has only

a trivial solution and therefore there are no fundamental solutions.





140

3 Systems of Linear Equations

We will denote the general solution of the homogeneous system by Xgen.

Xgen. = C1X1 + C2X2 + · · · + C − X − ,

:

(3.65)

n

r

n r

where C , C , . . . , C

are arbitrary constants.

1

2

n−r

Example 3.6 Find the fundamental system of solutions for the homogeneous

system of equations

⎧

⎪

2x1 − 4x2 + 5x3 + 3x4 = 0

⎪

,

⎨

3x − 6x + 4x + 2x = 0,

(3.66)

(3.67)

1

2

3

4

⎪

⎪

⎩

4x − 8x + 17x + 11x = 0.

1

2

3

4

**Solution** Find the rank of the matrix of the given system

⎡

⎤

2 −4 5 3

3 −6 4 2

4 −8 17 11

⎢

⎥

⎢

⎥

,

⎣

⎦

by bringing it to the upper triangular form.

Subtract from the third row the second one. As a result we obtain

⎡

⎤

2 −4 5 3

3 −6 4 2

1 −2 13 9

⎢

⎥

⎢

⎥

(3.68)

(3.69)

,

⎣

⎦

permute the ﬁrst and the third rows:

⎡

⎤

1 −2 13 9

3 −6 4 2

2 −4 5 3

⎢

⎥

⎢

⎥

.

⎣

⎦

Subtract from the second row the ﬁrst row multiplied by 3, and from the third

row—the doubled ﬁrst row. We have

⎡

⎤

1 −2 13

9

⎢

⎥

⎢

⎥

(3.70)

0 0 −35 −25

0 0 −21 −15

.

⎣

⎦





3.4 Fundamental System of Solutions of Homogeneous Systems

141

Divide the second row by (−5), and the third one by (−3):

⎡

⎤

1 −2 13 9

0 0 7 5

0 0 7 5

⎢

⎥

⎢

⎥

(3.71)

.

⎣

⎦

⎤

Subtract from the third row the second one:

⎡

1 −2 13 9

0 0 7 5

⎢

⎥

⎢

⎥

(3.72)

.

⎣

⎦

0 0 0 0

From this we see that the rank of this matrix is equal to two.

As a basic non-zero minor, take, for example, the minor M31,,42 of the initial matrix:




5 3


(3.73)

.


4 2

Then, use the ﬁrst two equations, whose coefﬁcients are included into the basic

minor. Rearrange to the right side of the equations the summands that are not

included into the basic minor. We obtain

⎧

⎨

5x + 3x = 4x − 2x ,

3

4

2

1

(3.74)

(3.75)

(3.76)

⎩

4x + 2x = 6x − 3x .

3

4

2

1

Set two different values to the free unknowns x and x . The ﬁrst case:

1

2

⎡

⎤

⎡ ⎤

x1

x2

1

⎣

⎦ = ⎣ ⎦

.

0

Substituting these values into the system, we obtain

⎧

⎨

5x + 3x = −2,

3

4

⎩

4x + 2x = −3.

3

4

5

7

2

Solution of this system: x3 = − and x4 =

.

2





142

3

Systems of Linear Equations

The second case:

⎡

⎣

⎤

⎡ ⎤

x1

x2

0

⎦ = ⎣ ⎦

(3.77)

.

1

Similarly to the ﬁrst case, we obtain

⎧

⎨

5x + 3x = 4,

3

4

(3.78)

(3.79)

⎩

4x + 2x = 6.

3

4

While x = 5 and x = −7.

3

4

For the fundamental system of solutions we ﬁnally have

⎡

⎢

⎤

⎥

⎧⎡

⎤ ⎡ ⎤⎫

⎪

1

0

0

⎪

x1

⎪

⎪

⎪

⎪

⎪⎢

⎥ ⎢ ⎥⎪

⎪

⎪

⎢

⎥

⎨⎢

⎥ ⎢ ⎥⎬

1

⎢x2⎥

⎢

⎥ ⎢

⎥

∈

,

.

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎪⎢

⎥ ⎢ ⎥⎪

⎪ −5/2

5

⎪

x3

x4

⎣

⎦

⎪⎣

⎦ ⎣ ⎦⎪

⎪

⎪

⎪

⎪

⎩

⎭

7/2

−7

The general solution of this homogeneous system may be written as

⎡

⎤

⎡

⎤

2

0

0

1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

Xgen. = C1 ⎢ ⎥ + C2 ⎢ ⎥ ,

(3.80)

⎢

⎥

−5

⎢

⎥

−7

5

⎣

⎦

⎣

⎦

7

where C and C are arbitrary numbers.

1

2

**3.5 General Solution of the Non-homogeneous System**

**of Equations**

Consider a non-homogeneous system of equations:

⎧

⎪

\+

\+ · · · +

\=

⎪ a x

a x

12

a x

1n

1

b ,

⎪

11

1

2

n

⎪

⎪

⎨

a21x1 + a22x2 + · · · + a2 x = b2,

n

n

(3.81)

⎪

⎪ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎪

⎪

⎪

⎩

a

m

1x1 + a 2x2 + · · · + a x = b .

m

mn

n

m





3.5 General Solution of the Non-homogeneous System of Equations

143

**Theorem 3.5** Let Xgen. be the general solution of the homogeneous system, when

all the values bi are replaced with zeroes, and Xspec. is the particular solution of the

non-homogeneous system. Then, X, the general solution of the non-homogeneous

system, is equal to

X = Xgen. + Xspec.

Example 3.7 Solve the system:

.

(3.82)

⎧

⎪

2

\+

−

x4

− 3 = 2

⎪

x1 x2 x3

,

⎪

⎪

⎪

⎨

4x + x − 7x = 3,

1

3

4

(3.83)

⎪

⎪

2x − 3x + x = 1,

⎪

2

3

4

⎪

⎪

⎩

2x + 3x − 4x − 2x = 3.

1

2

3

4

**Solution** Write the augmented system matrix:

⎡

⎤

2 1 −1 −3 | 2

⎢

⎥

⎢

⎥

4 0 1 −7 | 3

0 2 −3 1 | 1

2 3 −4 −2 | 3

⎢

⎥

(3.84)

⎢

⎥ .

⎢

⎥

⎣

⎦

Find the rank of this matrix, for which purpose subtract from the second row the

doubled ﬁrst row, and from the fourth row—the ﬁrst row:

⎡

⎤

2 1 −1 −3 | 2

0 −2 3 −1 | −1

0 2 −3 1 | 1

0 2 −3 1 | 1

⎢

⎥

⎢

⎥

⎢

⎥

(3.85)

⎢

⎥ .

⎢

⎥

⎣

⎦

One can see that the last three rows are proportionalto each other, and it is enough

to keep one of them:

⎡

⎣

⎤

⎦

2 1 −1 −3 | 2

0 −2 3 −1 | −1

.

(3.86)





144

3 Systems of Linear Equations

The rank of the basic and the augmented matrices is equal to two, therefore,

the system is consistent. Find the general solution of the homogeneous system, for

which purpose rearrange x and x to the right side of the equations. We obtain

3

4

⎧

⎨

2x + x = x + 3x ,

1

2

3

4

(3.87)

(3.88)

(3.89)

⎩

−2x = −3x + x .

2

3

4

Select the following values for the independent variables:

⎡

⎤

⎡ ⎤

x3

x4

1

⎣

⎦ = ⎣ ⎦

,

0

in such a case, we obtain the system

⎧

⎨

2x + x = 1,

1

2

⎩

−2x2 = −3,

3

1

4

whence x = , x = − .

2

1

2

Now, selecting the values

⎡

⎣

⎤

⎡ ⎤

x3

x4

0

⎦ = ⎣ ⎦

(3.90)

(3.91)

,

1

we obtain the system

⎧

⎨

2x + x = 3,

1

2

⎩

−2x2 = 1,

1

7

whose solution is x = − and x =

.

2

1

2

4

Therefore, the general solution of the homogeneous system has the form:

⎡

⎤

⎡

⎤

1

7

−

⎢

4⎥

⎢ 4 ⎥

⎢

⎥

⎢

⎥

⎢ 3 ⎥

⎢

1⎥

⎢

⎥

⎢− ⎥

Xgen. = C1 ⎢ 2 ⎥ + C2 ⎢ 2⎥ , where C1, C2 ∈ R.

(3.92)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

0

⎣

⎦

⎣

⎦

0

1





Review Questions

145

If we introduce for consideration new constants C = C /4, C = C /4, then

1

2

1

2

Xgen. will be written in the form, free from fractions:

⎡

⎤

⎡

⎤

−1

7

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

6

−2

0

⎢

⎥

⎢

⎥

1

2

1

2

Xgen. = C ⎢ ⎥ + C ⎢ ⎥ , where C , C ∈ R.

(3.93)

⎢

⎥

⎢

⎥

4

⎣

⎦

⎣

⎦

0

4

In order to ﬁnd the particular solution, return to the augmented matrix ([3.86](#br156)).

The equations for computation of Xspec. have the form:

⎧

⎨

2x + x = x + 3x + 2,

1

2

3

4

(3.94)

⎩

−2x = −3x + x − 1.

2

3

4

Assuming that the values of the independent variables are equal to zero, we ﬁnd

3

1

x1 = , x2 = , and

4

2

⎡ ⎤

3

⎢4⎥

⎢1⎥

⎢ ⎥

Xspec. =

⎢ ⎥

2

.

(3.95)

⎢ ⎥

⎢ ⎥

0

⎣ ⎦

0

As a result, the general solution of the non-homogeneous system is equal to

⎡

⎤

⎡

⎤

⎡ ⎤

−1

7

−2

0

3

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

⎢ ⎥

6

1

2

⎢

⎥

⎢

⎥

⎢ ⎥

1

2

1

2

X = Xgen. + Xspec. = C ⎢ ⎥ + C ⎢ ⎥ + ⎢ ⎥ , where C , C ∈ R.

⎢

⎥

⎢

⎥

4 ⎢ ⎥

4

0

⎣

⎦

⎣

⎦

⎣ ⎦

0

4

0

(3.96)

**Review Questions**

\1. Deﬁne solution of a system of linear equations.

\2. What system of equations is called consistent? inconsistent?





146

3 Systems of Linear Equations

\3. When is the system of equations deﬁnite? indeﬁnite?

\4. Explain how an augmented matrix of a system of linear equations constructed.

\5. Describe the methods of solving the systems of linear equations: Gaussian

method, inverse matrix method, Cramer’s method.

\6. What is the complexity of the Gaussian method?

\7. What solution does any homogeneous system of linear equations have?

\8. Deﬁne the fundamental system of solutions.

\9. How is the general solution of a non-homogeneous system computed?

**Problems**

**3.1**. In order to expand a computer laboratory, its chief is planning to purchase

9 workstations and 7 notebooks. If 14 workstations and 9 notebooks are

ordered, the cost of the purchase will grow by 1.5 times. Find how many

times the workstation is more expensive than the notebook.

**3.2**. Solve the system of linear equations using Cramer’s rule:

⎧

⎧

⎨

⎪2

−

\+ 3x3

\=

9

,

⎪ x1 x2

⎨

3x − 5y = 13,

2x + 7y = 81;

(a)

(b) 3x − 5x − x = −10,

1

2

3

⎩

⎪

⎪

⎩

4x − 7x + x = −7;

1

2

3

⎧

⎧

⎪

\+ 2 + = 4

⎪2 − 4 + 9 = 28

⎪

x

y

z

,

⎪ x

y

z

,

⎨

⎨

(c) 3x − 5y + 3z = 1, (d) 7x + 3y − 6z = −1,

⎪

⎪

⎪

⎪

⎩

⎩

2x + 7y − z = 8;

7x + 9y − 9z = 5;

⎧

⎧

⎪

7 + 2 + 3 = 15

⎪

\+

\+

\=

36

,

⎪

x

y

z

,

⎪x

y

z

⎨

⎨

(e)

5x − 3y + 2z = 15, (f )

10x − 11y + 5z = 36;

2x − 3z = −17,

⎪

⎪

⎪

⎪

⎩

⎩

6x − 5z =

7;

⎧

⎪ 3 + 2x2

\+

= 5

⎪ x1

x3

,

⎨

(g)

x + x − x = 0,

1

2

3

⎪

⎪

⎩

4x − x + 5x = 3.

1

2

3





Problems

147

**3.3**. Solve the system of linear equations using Gaussian elimination:

⎧

⎧

⎪6 + 2x2 + 3x3 = 74

⎪ 2 + 5x2 − 2x3 = −6

⎪ x1

,

⎪

x1

,

⎨

⎨

(a)

7x + 4x = 91, (b) −3x − 2x + x = 0,

x1 + x2 + x3 = 18;

1

2

1

2

3

⎪

⎪

⎪

⎪

⎩

⎩

3x2 + 2x3 = −8;

⎧

⎧

⎪

3x1

−

\+ 6x3 = −4

⎪

5x1 + 3x2 − 3x3

\=

8

,

⎪

x2

,

⎪

⎨

⎨

(c)

3x − 7x =

2, (d) −4x − 3x − 2x =

1,

1

2

1

2

3

⎪

⎪

⎪

⎪

⎩

⎩

−4x − 4x − 3x = −10;

−2x + 3x + 6x = −29.

1

2

3

1

2

3

**3.4**. Solve the system of linear equations using Gaussian elimination:

⎧

⎧

⎪

⎪

⎪

−2x1 + 7x2 + 4x3 = 32

⎪

−x1 − 2x3

−

= −6

⎪

,

⎪

x4

,

⎪

⎪

⎪

⎪

⎪

⎪

⎨

⎨

2x + 8x − x + 7x = 63,

−5x − x + 6x + x = 23,

1

2

3

4

1

2

3

4

(a)

(b)

⎪

⎪

⎪−6 + 6x2 + 8x3 − 8x4 = 2

⎪5 − 8x2 − 9x3 + 4x4 = 62

⎪

x1

,

⎪ x1

,

⎪

⎪

⎪

⎪

⎪

⎪

⎩

⎩

6x − 4x + 5x = 58;

6x − 9x − 5x + x = 73;

2

3

4

1

2

3

4

⎧

⎧

⎪

⎪

⎪

4x1 − 9x3

−

\=

37

,

⎪ −8

\+

− 4x3 − 8x4

\=

7

,

⎪

x4

⎪

x1 x2

⎪

⎪

⎪

⎪

⎪

⎪

⎨

⎨

7x − x − 5x − 5x = 36,

−7x − 6x + 7x = 56,

1

2

3

4

2

3

4

(c)

(d)

⎪

⎪

⎪

8x1 − 5x2 + 4x4 = −38

⎪−8 + 3x2 + 2x3 − 2x4 = −63

⎪

,

⎪

x1

,

⎪

⎪

⎪

⎪

⎪

⎪

⎩

⎩

x1 − 4x2 + 9x3 − 4x4 = −25;

−8x1 − 3x2 − x3 − 4x4 = −6.

∗**3.5.** Solve the system of linear equations relative to ﬁve unknowns:

⎧

⎪

⎪

5x − 8x − 5x + 8x + 8x = −5,

⎪

1

2

3

4

5

⎪

⎪

⎪

⎪

2

\+ 2x3

\+

−

\=

8

,

⎪

x2

x4 x5

⎨

(a) −2x + 4x + 3x − 8x + 4x = −39,

1

2

3

4

5

⎪

⎪

⎪

⎪

5

\+ 6 + 2 − 2 − 4

\=

32

,

⎪

x1

x2

x3 x4

x5

⎪

⎪

⎪

⎩

x1 − 2x2 − x3 + 2x4 − 2x5 = 23;

⎧

⎪

⎪

6x − x + 6x + 3x − 7x =

6,

⎪

1

2

3

4

5

⎪

⎪

⎪

⎪−4 − 4x2 + 3x3

−

− 8x5 = −30

⎪

x1

x4

,

⎨

(b)

−x + x + 5x − x = −22,

1

2

4

5

⎪

⎪

⎪

⎪

4

x1 x2

\+

− 3 + 3 − 5 = −3

⎪

x3

x4 x5

,

⎪

⎪

⎪

⎩

8x + x − x = −61.

2

4

5





148

3 Systems of Linear Equations

∗**3.6.** Solve the system of linear equations relative to six unknowns:

⎧

⎪

⎪

−x + 2x + 5x − 2x − 4x =

4,

⎪

1

3

4

5

6

⎪

⎪

⎪

⎪−

−

\+

− 3

\+

− 4 = −46

⎪

x1 x2 x3

x4 x5

x6

,

⎪

⎪

⎪

⎨

−x + 5x + 4x − 2x − x = −19,

1

2

3

5

6

(a)

⎪

⎪

x − 2x + 4x − 2x − x = −9,

⎪

1

2

3

5

6

⎪

⎪

⎪

⎪ −2 − 5 + 3 − 2 − 3 = −20

⎪

x1

x2

x3

x4

x5

,

⎪

⎪

⎪

⎩

3x + x + 3x + x =

4;

1

2

3

6

⎧

⎪

⎪

−2x − 4x − 4x + 5x =

2,

⎪

1

2

5

6

⎪

⎪

⎪

⎪

−

\+ 5 + 3 + 5 = −12

⎪

x1

x2 x3

x5

,

⎪

⎪

⎪

⎨

−2x − 5x + 5x − 3x − 5x − 3x = −7,

1

2

3

4

5

6

(b)

⎪

⎪−4x − 5x − 3x + 5x − 2x + 3x = 10,

⎪

1

2

3

4

5

6

⎪

⎪

⎪

⎪

\+ 3 − 5 + 4 + 3 + 2

\=

8

,

⎪

x

x

x

x

x

5

x

⎪

1

2

3

4

6

⎪

⎪

⎩

−4x + x − 4x + 3x + x − x =

\3.

1

2

3

4

5

6

**3.7**. Find the fourth power polynomial p(x) with real coefﬁcients, for which the

following properties are valid: p(5) = 1 and p(1) = p(2) = p(3) =

p(4) = 0.

**3.8**. At what values of the parameter λ is the system of equations

⎧

⎪

\+

= 1

⎪ x1 x2

,

⎨

λx1 + x2 = 2,

x1 + λx2 = 4.

⎪

⎪

⎩

consistent?

**3.9**. At what values of the parameter λ does the system of linear equations

⎧

⎪

\+

\=

0

,

⎪

x1 λx2

⎨

−x + x − x = 5,

1

2

3

⎪

⎪

⎩

−x + x = −4,

2

3

have the unique solution? With these values of λ, ﬁnd the solution of the

system using Cramer’s rule.





Problems

149

∗**3.10.** Solve the matrix equation A · X · B = C, where

⎡

⎤

⎡

⎤

⎡

⎤

−3 2 3

−13 0

−25 0

−33 0

⎢

⎥

−1 0

−1 0

⎢

⎥

A = −2 1 4 , B

⎢

⎥

= ⎣

⎦

, C

= ⎢

⎥

.

(3.97)

⎣

⎦

⎣

⎦

6 1 2

Note the degeneracy of one of the multipliers, namely the matrix B.

∗**3.11.** Solve the matrix equations:

⎡

⎤

⎡

⎤

6 2

−4 4

−2 2

(1) ⎣ ⎦ · X = ⎣

⎦ ;

3 1

⎡

⎤

⎡

⎤

15 −5

−3 1

1 −1

−2 1

(2) X · ⎣

⎦ = ⎣

⎦ ;

⎡

⎤

⎡

⎤

6

−1 1

6

19 −22

⎢

⎥

⎢

⎥

(3) X · ⎢−10 −5 6 ⎥ = ⎢10

−6 ⎥ ;

5

⎣

⎦

⎣

⎦

0

−20 23

−6 −19 22

−7 8 2

⎡

⎤

⎡

⎤

−1 2

⎣

5

⎢

⎥

⎢

⎥

(4) ⎢ 5

−1 ⎥ · X = ⎢ 2 7 1⎥ .

3

⎦

⎣

⎦

7 −1 −11

1 −1 1

**3.12**. A program code is given that processes the one-dimensional array a,

consisting of ﬁve elements:

for i in range(len(a)):

temp = a[0]

for j in range(len(a) - 1):

a[j] = -2

a[j + 1]

\*

a[len(a) - 1] += temp

After executing this program code segment, the array a[] consists of

the following elements: [-32, 32, 32, 32, 16]. Find what values

the elements of the array a[i], where i = 1, . . . , 5, before executing this

segment.

**3.13**. A program code is given that processes the one-dimensional array a,

consisting of seven elements:

for i in range(len(a)):

temp = a[0]





150

3 Systems of Linear Equations

for j in range(len(a) - 1):

a[j] = 3 a[j + 1] - 1

\*

a[len(a) - 2] = -a[len(a) - 2] - temp

After executing this program code segment, the array a[] consists of the

following elements: [365, 608, -769, -499, -409, 107, 5].

Find what values the elements of the array a[i], i = 1, . . . , 7 took before

executing this segment.

**3.14**. There [ex](#br163)ists a modiﬁcation of Gaussian elimination referred to as **Gauss–**

**Jorda[n**](#br163)[**5](#br163)[ ](#br163)elimination**. In the Gauss–Jordan method, the coefﬁcient matrix

is brought not to a triangular, but to a diagonal form. Write the realization

of this method in Python and compare its asymptotic complexity with the

complexity of the standard Gaussian elimination.

**3.15**. Find the general solution and the fundamental system of solutions for the

systems of equations:

⎧

⎧

⎪

− 4x2

\+

−

= 0

⎪ 2

−

\+ 3x3

\+

−

= 0

= 0

⎪ x1

x3

,

⎪

x1 x2

x4

x3

,

,

⎨

⎨

(1)

\+

= 0 (2)

2x1 − 5x2

x1 x2 x3

,

⎪

⎪

⎪

⎪

⎩

⎩

3x − 2x − x = 0;

4x − 7x + x + 3x = 0;

1

2

3

1

2

3

4

⎧

⎧

⎪

\+ 2 + 4 − 3 = 0

⎪3 + 5 + 2 = 0

⎪

x1

x2

x3

x4

,

⎪ x

x2

x3

,

⎪

⎪

1

⎪

⎪

⎪

⎪

⎨

⎨

3x + 5x + 6x − 4x = 0,

4x + 7x + 5x = 0,

1

2

3

4

1

2

3

(3)

(4)

⎪

⎪

⎪

4x + 5x − 2x + 3x = 0,

⎪

x + x − 4x = 0,

⎪

1

2

3

4

⎪

1

2

3

⎪

⎪

⎪

⎪

⎩

⎩

⎧

3x + 8x + 24x − 19x = 0;

2x + 9x + 6x = 0;

1

2

3

4

1

2

3

⎧

⎪2 + 4 + 6

\+

= 0

⎪ x

x2

x3 x4

,

⎪

1

⎪

⎪

\+ 2 + 3 = 0

⎪

⎪ x

y

z

,

,

⎨

⎨

x1 + 2x2 + 3x3 + x4 = 0,

(5)

(6) 2 + 3 + 4 = 0

x

y

z

z

⎪

⎪

⎪3x + 6x + 9x − x = 0,

⎪

⎪

1

2

3

4

⎩

⎪

\+

\+

= 0;

⎪

x

y

⎩

x1 + 2x2 + 3x3 + 5x4 = 0;

⎧

⎪

− 2 + 3 − 4 = 0

2x − 4x + 5x + 7x = 0,

⎪

x1

x2

x3 x4

,

⎪

⎪

⎪

⎨

1

2

3

4

(7)

⎪

⎪ 6x − 12x + 17x − 9x = 0,

⎪

1

2

3

4

⎪

⎪

⎩

7x − 14x + 19x + 17x = 0.

1

2

3

4

5Wilhelm Jordan (1842–1899), German geodesist and mathematician.





Answers and Solutions

151

**Answers and Solutions**

[**3.1**](#br159)[** ](#br159)Solution.

Denote the price of one workstation by x, and of one notebook—by y. Assume

that the cost of 9 workstations and 7 notebooks is a. Then, we obtain a system of

linear equations relative to the unknowns x and y:

⎧

⎨ 9 + 7 =

x

y

a,

3

⎩14 + 9 =

x

y

a.

2

3

1

Its solution is x =

a, y =

a. Therefore, the workstation is three times more

34

34

expensive than the notebook.

[**3.2**](#br159)[** ](#br159)Solution.

(a) The augmented matrix of the system has the form

⎡

⎤

3 −5 | 13

2 7 | 81

⎣

⎦.

Compute the required determinants:




3 −5

` `=

` `= 21 + 10 = 31,


2 7 




13 −5

x =

` `= 91 + 405 = 496.


81 7 

496

31

x

Therefore, x =

\=

= 16.





3 13

y =

` `= 243 − 26 = 217,


2 81

217

y

y =

\=

= 7.

31

(b) The augmented matrix of the system has the form

⎡

⎤

2 −1 3 |

9

⎢

⎥

⎢

⎥.

3 −5 −1 | −10

⎣

⎦

4 −7 1 | −7









2 −1 3

11 −16 0

3 −5 −1








` `= 3 −5 −1

` `=(1)+3(2) 

` `= 11 · −12 + 16 · 7 = −20,

(

)







4 −7 1 

` `4 −7 1 





152

3 Systems of Linear Equations












9

−1 3

−21 −16 0

−10 −5 −1








1 = −10 −5 −1

` `=(1)+3(2) 

` `=(3)+(2)




` `−7 −7 1 

` `−7 −7 1 




−21 −16 0




= −10 −5 −1 = 252 − 272 = −20,




−17 −12 0 

1

−20

−20

3

x1 =

\=

= 1,










2

9

11 −21 0

3 −10 −1









` `=(1)+3(2) 

` `=(3)+(2)

2 = 3 −10 −1







4 −7 1 

` `4 −7 1 




11 −21 0




=  3 −10 −1 = −(−1)(−187 + 147) = −40,




` `7 −17 0 

2

−40

−20

9

x2 =

\=

= 2,










2 −1

0

−1

9








3 = 3 −5 −10

` `=[1]+2[2] 

−7 −5 −10








4 −7 −7 

−10 −7 −7 

= (49 − 100) + 9(49 − 50) = −60,

3

−60

−20

x3 =

\=

= 3.

(c) The augmented matrix of the system has the form

⎡

⎤

1 2 1 | 4

3 −5 3 | 1

2 7 −1 | 8

⎢

⎥

⎢

⎥.

⎣

⎦










1 2

1

0 2

1








` `= 3 −5 3

` `=[1]−[3] 

0 −5 3

` `= 3 · 6 + 5 = 33,

(

)






2 7 −1

3 7 −1









4 2

1

4 2

1








` `= 1 −5 3

` `=(3)−2(1) 

= 1,

1 −5 3

` `= 4 · 15 − 9 − −6 − 3 = 33,

(

)

(

)

x







8 7 −1

0 3 −3

33

33

x

x =

\=





Answers and Solutions

153








1 4 1

1

0

1








` `= 3 1 3

` `=[2]−4[1] 

= 1,

3 −11 3

` `= −11 · −1 − 2 = 33,

(

)

y








2 8 −1

2

0

−1

33

y

y =

\=

33









1 2 4

1 2 4








` `= 3 −5 1

` `=(3)−2(1) 

3 −5 1

` `= −3 · 1 − 12 = 33,

(

)

z







2 7 8

0 3 0

33

33

z

z =

\=

= 1.

(d) The augmented matrix of the system has the form

⎡

⎤

2 −4 9 | 28

7 3 −6 | −1

7 9 −9 | 5

⎢

⎥

⎢

⎥.

⎣

⎦









2 −4 9

2 −4 9

7 3 −6








` `= 7 3 −6

` `=(3)−(2) 

` `= 2 −9 + 36 − 7 12 − 54 = 348,

(

)

(

)







7 9 −9

0 6 −3










28 −4 9

33 5 0









` `=(1)+(3) 

` `= 6 297 − 25 − 9 99 + 5 = 696,

` `= −1 3 −6

−1 3 −6

(

)

(

)

x






` `5 9 −9

` `5 9 −9

696

x =

= 2,

348








2 28 9

2 28 9








` `= 7 −1 −6

` `=(3)−(2) 

7 −1 −6

` `= 2 3 + 36 − 7 −84 − 54 = 1044,

(

)

(

)

y








7 5 −9

0 6 −3

1044

y =

= 3,

348









2 −4 28

2 −4 28

7 3 −1








` `= 7 3 −1

` `=(3)−(2) 

` `= 2 18+6 −7 −24−168 = 1392,

(

)

(

)

z







7 9 5 

0 6 6 

1392

z =

= 4.

348





154

3 Systems of Linear Equations

(e) The augmented matrix of the system has the form

⎡

⎤

7

2

3 | 15

⎢

⎥

⎢

⎥.

5 −3 2 | 15

⎣

⎦

10 −11 5 | 36










7

2

3

7 2 3








` `= 5 −3 2

` `=(3)−2(2) 

5 −3 2

` `= 5 14 − 15 + −21 − 10 = −36,

(

)

(

)






10 −11 5

0 −5 1








15

2

3

15

2

3








` `= 15 −3 2

` `=(2)−(1) 

0 −5 −1

` `= −72,

x








36 −11 5

36 −11 5 

−72

x =

= 2,

−36











7 15 3

7 15 3








` `= 5 15 2

` `=(2)−(1) 

−2 0 −1

` `= 2 75 − 108 + 252 − 150 = 36,

(

)

(

)

y





10 36 5

10 36 5 

36

y =

= −1,

−36




7

2 15




` `= 5 −3 15

` `= −36,

z




10 11 36

−36

z =

= 1.

−36

(f) The augmented matrix of the system has the form

⎡

⎤

1 1 1 | 36

2 0 −3 | −17

6 0 −5 |

⎢

⎥

⎢

⎥.

⎣

⎦

7




1 1 1




` `= 2 0 −3

` `= − −10 + 18 = −8,

(

)




6 0 −5




36 1 1




` `= −17 0 −3

` `= − 85 + 21 = −106,

(

)

x




` `7 0 −5

−106

53

4

x =

\=

.

−8





Answers and Solutions

155









1 36

1

1 36

1








(3)−3(2)

` `= 2 −17 −3 = 2 −2 1 0 −89 −5



` `= −356 + 290 = −66,

y


( ) ( ) 




6

−66

−8

7

−5

0 58 4 

33

y =

\=

,

4




1 1 36




` `= 2 0 −17

` `= − 14 + 17 · 6 = −116,

(

)

z




6 0 7 

−116

29

z =

\=

.

−8

2

(g) The augmented matrix of the system has the form

⎡

⎤

3 2 1 | 5

1 1 −1 | 0

4 −1 5 | 3

⎢

⎥

⎢

⎥.

⎣

⎦















3 2

1

1 2

1

1 2 3












` `= 1 1 −1

` `=[1]−[2] 

0 1 −1

` `=[3]+[2] 

0 1 0

` `= 4 − 15 = −11,









4 −1 5 

5 −1 4 

5 −1 4










5 2

1

5 2 3

0 1 0









` `=[3]+[2] 

= −1.

` `= 20 − 9 = 11

1 = 0 1 −1

,






3 −1 5 

3 −1 4

11

x1 =

−11









3 5 1

4 5 1








2 = 1 0 −1

` `=[1]+[3] 

0 0 −1

` `= 12 − 45 = −33,







4 3 5 

9 3 5 

−33

x2 =

= 3,

−11









3 2 5

1 2 5








3 = 1 1 0

` `=[1]−[2] 

0 1 0

` `= 3 − 25 = −22,







4 −1 3

5 −1 3

−22

x3 =

= 2.

−11





156

3 Systems of Linear Equations

[**3.3**](#br160)[** ](#br160)Solution.

(a) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

6 2 3 | 74

7 4 0 | 91

1 1 1 | 18

0 −4 −3 | −34

0 −3 −7 | −35

1 1 1 | 18

⎢

⎥

(1)−6(3) ⎢

⎥

⎢

⎥ →(2)−7(3) ⎢

⎥ →−3·(1)

⎣

⎦

⎣

⎦

⎡

⎤

⎡

⎤

0 12 9 | 102

0 0 −19 | −38

⎢

⎥

⎢

⎥

→ ⎢0 −3 −7 | −35⎥ →(

1)+4(2) ⎢

0 −3 −7 | −35 .

⎥

⎣

⎦

⎣

⎦

1 1 1 | 18

1 1

1

| 18

38

19

Hence it follows that x =

= 2,

3

−3x = −35 + 14 = −21, x = 7,

2

2

x1 = 18 − 2 − 7 = 9.

The ﬁnal answer is [x , x , x ]T = [9, 7, 2]T .

1

2

3

(b) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

2

5 −2 | −6

2

5 −2 | −6

⎢

⎥

⎢

⎥

⎢

⎥ →2·(2) ⎢

⎥ →(2)+3(1)

−3 −2 1 | 0

0

−6 −4 2 | 0

0

⎣

⎦

⎣

⎦

3

2 | −8

3

2 | −8

⎡

⎤

⎡

⎤

2 5 −2 | −6

2 5 −2 | −6

⎣

⎢

⎥

⎢

⎥

→ ⎢0 11 −4 | −18⎥ →11·(3) ⎢0 11 −4 | −18⎥ →(3)−3(2)

⎣

⎦

⎤

⎦

0 3 2 | −8

2 5 −2 | −6

0 33 22 | −88

⎡

⎢

⎥

→ ⎢0 11 −4 | −18⎥.

⎣

⎦

0 0 34 | −34

−34

Hence it follows that x =

= −1,

3

34

11x = −18 − 4 = −22, x = −2,

2

2

2x = −6 − 2 + 10 = 2, x = 1.

1

1

We obtain the answer: [x , x , x ]T = [1, −2, 1]T .

1

2

3





Answers and Solutions

157

(c) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

3 −1 6 | −4

3 −1 6 | −4

⎢

⎥

⎢

⎥

⎢

⎥ →(2)−(1) ⎢

⎥ →4·(1)

3 −7 0 |

2

0 −6 −6 |

6

⎣

⎦

⎤

⎣

⎦

−4 −4 −3 | −10

−4 −4 −3 | −10

0 −16 15 | −46

⎡

⎡

⎤

12 −4 24 | −16

⎢

⎥

⎢

⎥

→ ⎢ 0 −6 −6 | 6 ⎥ →(1)+3(3) ⎢ 0 −6 −6 | 6 ⎥ →(2)·8

⎣

⎡

⎦

⎣

⎦

−4 −4 −3 | −10

−4 −4 −3 | −10

⎤

⎡

⎤

0 −16 15 | −46

0 −16 15 | −46

⎢

⎥

⎢

⎥

(1)↔(2)

→ ⎢ 0 −48 −48 | 48 ⎥ →(2)−3(1) ⎢ 0

−93 | 186⎥ →(3)↔(1)

0

⎣

⎡

⎦

⎣

⎦

−4 −4 −3 | −10

−4 −4 −3 | −10

−4 −4 −3 | −10

⎤

⎢

⎥

→ ⎢ 0 −16 15 | −46⎥.

⎣

⎦

0

0

−93 | 186

Hence it follows that x = −2,

3

−16x = −46 + 30 = −16, x = 1,

2

2

−4x = −10 − 6 + 4 = −12, x = 3.

1

1

We obtain the answer: [x , x , x ]T = [3, 1, −2]T .

1

2

3

(d) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

5

3 −3 |

8

1

5

3

−3 |

8

⎢

⎥

⎢

⎥

⎢

⎥ →(2)−2(3) ⎢

⎥ →2·(1)

−4 −3 −2 |

−2 3 6 | −29

10 6 −6 | 16

0 −9 −14 | 59

⎣

⎦

⎣

⎦

−2 3

6

| −29

0 21 24 | −129

⎡

⎢

⎤

⎡

⎤

⎥

⎢

⎥

1

3

→ ⎢ 0 −9 −14 | 59 ⎥ →(1)+5(3) ⎢ 0 −9 −14 | 59 ⎥ → (

\1)

⎣

⎡

⎦

⎣

⎦

−2 3

0

6

8

| −29

| −43

−2 3

0

6

8

| −29

⎤

⎡

⎤

7

7

| −43

⎢

⎥

⎢

⎥

→ ⎢ 0 −9 −14 | 59 ⎥ →7·(2)= ⎢ 0 −63 −98 | 413⎥ →(2)+9(1)

⎣

⎡

⎦

⎣

⎦

−2 3

0 7

6

| −29

−2

3

6

| −29

⎤

⎡

⎤

8

| −43

−2 3

6

| −29

⎢

⎥

(1)↔(3) ⎢

⎥

→ ⎢ 0 0 −26 | 26 ⎥ →(3)↔(2) ⎢ 0 7

| −43⎥.

8

⎣

⎦

⎣

⎦

−2 3

6

| −29

0 0 −26 | 26





158

3 Systems of Linear Equations

Hence it follows that x = −1,

3

7x = −43 + 8 = −35, x = −5,

2

2

−2x = −29 + 6 + 15 = −8, x = 4.

1

1

We obtain the answer: [x , x , x ]T = [4, −5, −1]T .

1

2

3

[**3.4**](#br160)[** ](#br160)Solution.

(a) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

−2 7 4 0 | 32

2 8 −1 7 | 63

−3 3 4 −4 | 1

0 6 −4 5 | 58

0 15 3 7 | 95

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

2

8 −1 7 | 63

⎢

⎥

⎢

⎥

→(1)+(2)

⎢

⎥

⎢

⎢

⎥

⎢

−3 3 4 −4 | 1

⎣

⎦

⎣

0

⎡

⎤

⎡

2

8 −1 7 | 63

⎢

⎥

⎢

⎢

⎥

⎢

0 15 3 7 | 95

⎢

⎥

⎢

\=

→2(4)+3(1)

→2·(2)

⎢

⎥

⎢

⎢

⎥

⎢

0

6 −4 5 | 58

⎣

⎦

⎣

−3 3 4 −4 | 1

⎡

⎤

⎡

2 8 −1 7 | 63

0 30 6 14 | 190

0 6 −4 5 | 58

0 30 5 13 | 191

2 8 −1

7

1

5

⎢

⎥

⎢

⎢

⎥

⎢

(2)−(4) 0 0 1

⎢

⎥

⎢

→

→

→(4)−5(3)

→(4)−25(2)

⎢

⎥

⎢

⎢

⎥

⎢

0 6 −4

⎣

⎦

⎣

⎡

⎤

2 8 −1

0 6 −4

0 0 1

7

5

1

| 63

| 58

| −1

⎢

⎥

⎢

⎥

⎢

⎥

,

⎢

⎥

⎢

⎥

⎣

⎦

0 0 0 −37 | −74

−74

x4 =

= 2,

−37

x3 = −1 − 2 = −3,

6x = 58 − 12 − 10 = 36, x = 6,

2

2

2x = 63 − 48 − 3 − 14 = −2, x = −1.

1

1

Write the answer: [x , x , x , x ]T = [−1, 6, −3, 2]T .

1

2

3

4





Answers and Solutions

159

(b) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

−1 0 −2 −1 | −6

−5 −1 6 1 | 23

5 −8 −9 4 | 62

6 −9 −5 1 | 73

1

0

2 1 | 6

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

−5 −1 6 1 | 23

5 −8 −9 4 | 62

6 −9 −5 1 | 73

⎢

⎥

⎢

⎥

→(1)·(−1)

→(3)+(2)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦

⎡

⎤

⎡

⎤

1

0

2 1 | 6

1 0

2

1 | 6

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

−5 −1 6 1 | 23

0 −9 −3 5 | 85

6 −9 −5 1 | 73

(2)+5(1) 0 −1 16 6 | 53

⎢

⎥

⎢

⎥

→(4)−6(1)

→(4)−(3)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 −9 −3 5 | 85

0 −9 −17 −5 | 37

⎣

⎦

⎣

⎦

⎡

⎤

⎡

⎤

1 0

2

1

6

5

|

6

| 53

| 85

1 0 2 1 | 6

0 −1 16 6 | 53

0 −9 −3 5 | 85

0 0 7 5 | 24

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 −1 16

0 −9 −3

⎢

⎥

−1

2

⎢

⎥

\4)

→( ) ( )

3 −9 2

→

→

(

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦

0 0 −14 −10 | −48

⎡

⎤

⎡

⎤

1 0

2

1

|

|

6

1 0 2 1 | 6

0 −1 16 6 | 53

0 0 0 56 | 112

0 0 7 5 | 24

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 −1 16

6

53

⎢

⎥

⎢

⎥

→

→

→(3)+21(4)

→(3)↔(4)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 0 −147 −49 | −392

⎣

⎦

⎣

⎦

0 0

7

5

|

24

⎡

⎤

1 0 2 1 | 6

0 −1 16 6 | 53

0 0 7 5 | 24

⎢

⎥

⎢

⎥

⎢

⎥

,

⎢

⎥

⎢

⎥

⎣

⎦

0 0 0 56 | 112

112

x4 =

= 2,

56

7x = 24 − 10 = 14, x = 2,

3

3

−x = 53 − 12 − 32, x = −9,

2

2

x1 = 6 − 2 − 4 = 0.

Write the answer: [x , x , x , x ]T = [0, −9, 2, 2]T .

1

2

3

4





160

3 Systems of Linear Equations

(c) Execute the following elementary transformations of the augmented system

matrix:

(1)−4(4)

(2)−7(4)

3 −8 4

⎡

⎤

⎡

⎢

⎤

4 0 −9 −1 | 37

7 −1 −5 −5 | 36

8 −5 0 4 | −38

1 −4 9 −4 | −25

1 −4

9

−4 | −25

( ) ( )

(1)↔(2)

(1)↔(4)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 16 −45 15 | 137

0 27 −68 23 | 211

0 27 −72 36 | 162

⎢

⎥

⎢

⎥

1

9

·(4)

→(3)↔(4) =

→

⎢

⎥

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦

⎡

⎤

⎡

⎤

1 −4

9

−4 | −25

1 −4

9

−4 | −25

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 16 −45 15 | 137

0 27 −68 23 | 211

0 3 −8 4 | 18

0 16 −45 15 | 137

⎢

⎥

⎢

⎥

→

→

→

→(3)−9(4)

→3·(2)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 0

4

−13 | 49

⎣

⎦

⎣

⎦

0 3 −8

4

| 18

⎡

⎤

⎡

⎤

1 −4

9

−4 | −25

1 −4 9 −4 | −25

0 0 −7 −19 | 123

0 0 4 −13 | 49

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 48 −135 45 | 411

⎢

⎥

⎢

⎥

→(2)−16(4)

→4·(2)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 0

4

−13 | 49

⎣

⎦

⎣

⎦

0 3 −8

1 −4

4

| 18

0 3 −8

4

| 18

⎡

⎤

⎡

⎤

9

−4 | −25

1 −4 9 −4 | −25

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 0 −28 −76 | 492

(2)+7(3) 0 3 −8

4

| 18

−13 | 49

⎢

⎥

⎢

⎥

→(2)↔(4)

,

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 0

4

−13 | 49

0 0

4

⎣

⎦

⎣

⎦

0 3 −8

4

| 18

0 0 0 −167 | 835

835

x4 =

= −5,

−167

4x = 49 − 65 = −16, x = −4,

3

3

3x = 18 − 32 + 20 = 6, x = 2,

2

2

x1 = −25 + 8 + 36 − 20 = −1.

Write the answer: [x , x , x , x ]T = [−1, 2, −4, −5]T .

1

2

3

4

(d) Execute the following elementary transformations of the augmented system

matrix:

⎡

⎤

⎡

⎤

−8 1 −4 −8 |

7

−8 1 −4 −8 |

7

⎢

⎥

⎢

⎥

1

⎢

⎥

⎢

⎥

0 −7 −6 7 | 56

−8 3 2 −2 | −63

−8 −3 −1 −4 | −6

(3)−(1)

0 −7 −6 7 | 56

3

( )

⎢

⎥

⎢

⎥

→(4)−(1)

→2

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0

2

6

6 | −70

⎣

⎦

⎣

⎦

0 −4 3 4 | −13

⎡

⎤

⎡

⎤

−8 1 −4 −8 |

7

−8 1 −4 −8 |

7

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0 −7 −6 7 | 56

(2)+7(3)

0 0 15 28 | −189

0 1 3 3 | −35

0 0 15 16 | −153

⎢

⎥

⎢

⎥

→

→(4)+4(3)

→(4)−(2)

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

0

1

3

3 | −35

⎣

⎦

⎣

⎦

0 −4 3 4 | −13





Answers and Solutions

161

⎡

⎤

−8 1 −4 −8 |

7

⎢

⎥

⎢

⎥

0 0 15 28 | −189

⎢

⎥

→

,

⎢

⎥

⎢

⎥

0 1 3

3

| −35

⎣

⎦

0 0 0 −12 | 36

36

x4 =

= −3,

−12

15x = 84 − 189, x = −7,

3

3

x2 = −35 + 9 + 21 = −5,

−8x = 7 − 24 − 28 + 5 = −40, x = 5.

1

1

Write the answer: [x , x , x , x ]T = [5, −5, −7, −3]T .

1

2

3

4

[**3.5**](#br160)[** ](#br160)Answer:

(a) [x , x , x , x , x ]T = [6, −6, 7, 0, −6]T ;

1

2

3

4

5

(b) [x , x , x , x , x ]T = [6, −7, −1, −1, 4]T .

1

2

3

4

5

[**3.6**](#br161)[** ](#br161)Answer:

(a) [x , x , x , x , x , x ]T = [5, 0, −5, 5, −5, 4]T ;

1

2

3

4

5

6

(b) [x , x , x , x , x , x ]T = [1, −2, −2, 0, 1, 0]T .

1

2

3

4

5

6

[**3.7**](#br161)[** ](#br161)Solution.

The fourth power polynomial with real coefﬁcients can be presented in the form:

4

3

2

p(x) = a4x + a3x + a2x + a1x + a0,

where a , a , . . . , a ∈ R are the unknown coefﬁcients. We obtain system of linear

0

1

4

equations relative to the coefﬁcients a :

i

⎧

⎪

4

3

2

⎪5 a + 5 a + 5 a + 5a + a = 1,

⎪

4

3

2

1

0

⎪

⎪

⎪

⎪14 + 13 + 12 + 1

24a + 23a + 22a + 2a + a = 0,

\+

= 0

⎪

a4

a3

a2

a1 a0

,

⎨

4

3

2

1

0

⎪

⎪

⎪

⎪34 + 33 + 32 + 3

a1 a0

\+

= 0

⎪

a4

a3

a2

,

⎪

⎪

⎪

⎩

44a + 43a + 42a + 4a + a = 0.

4

3

2

1

0

Write the matrix of this system and bring it to the echelon form:

⎡

⎤

⎡

⎢

⎤

625 125 25 5 1 | 1

1 1 1 1 1 | 0

0 8 12 14 15 | 0

0 0 6 9 10 | 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

1

1 1 1 | 0

4 2 1 | 0

⎢

⎥

⎢

⎥

⎢

⎥

⎥

⎢

⎥ → ⎢

⎥

16

8

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢ 81 27 9 3 1 | 0⎥

⎢0 0 0 24 50 | 0⎥

⎣

⎦

⎣

⎦

256 64 16 4 1 | 0

0 0 0 0 1 | 1





162

3 Systems of Linear Equations

we ﬁnd the values of ai:

⎧

⎪

\=

= −

1

,

50

⎪ a0

⎧

⎪

⎪

⎪

⎪

⎪

⎪

a + a + a + a + a = 0,

⎪

⎪

4

3

2

1

0

⎪ a1

,

,

,

.

⎪

⎪

⎪

⎪

24

35

⎪

⎪

⎪8 + 12a2 + 14 + 15 = 0

⎪

⎪ a3

a1

a0

,

⎪

⎨

⎨

a2 =

6a + 9a + 10a = 0, ⇒

24

10

2

1

0

⎪

⎪

⎪

⎪

⎪

⎪

⎪

24 + 50 = 0

⎪

⎪

a1

a0

,

⎪

⎪

⎪

= −

⎪

⎪ a3

⎪

⎪

24

1

⎩

⎪

a0 = 1;

⎪

⎪

⎪

⎪

⎩

a4 =

24

As a result, the sought-for fourth power polynomial is equal to

1

4

3

2

p(x) =

(x − 10x + 35x − 50x + 24).

24

[**3.8**](#br161)[** ](#br161)Solution.

The system of linear equations is consistent if and only if the rank of the system

matrix is equal to the rank of the augmented system matrix.

Find the rank of the basic matrix:

⎡

⎤

1 1

⎢

⎥

A = λ 1

⎢

⎥

.

⎣

⎦

1 λ

⎡

⎤

⎡

⎤

1

1

1

1

(2)−λ(1) ⎢

⎥

⎢

⎥

3)+(2) ⎢

⎥

A → (

3)−(1) ⎢

0 1 − λ

⎥ → (

0 1 − λ

0

.

⎣

⎦

⎣

⎦

0 λ − 1

0

Therefore,

⎧

⎨

2, if λ = 1,

1, if λ = 1.

rk A =

⎩





Answers and Solutions

163

Compute the rank of the augmented matrix:

⎡

⎤

⎡

⎤

1 1 | 1

1

1

|

1

⎢

⎥

(2)−λ(1) ⎢

⎥

⎥ → (2)+(3)

(A|B) = λ 1 | 2

⎢

⎥ → (3)−(1) ⎢

0 1 − λ | 2 − λ

0 λ − 1 |

⎣

⎦

⎣

⎦

1 λ | 4

3

⎡

⎤

1

1

|

1

⎢

⎥

→ ⎢0 1 − | 2 − ⎥ .

λ

λ

⎣

⎦

0

0

| 5 − λ

Thus,

⎧

⎨

2, if λ = 5,

3, if λ = 5.

rk (A|B) =

⎩

The condition rk A = rk (A|B) is satisﬁed at λ = 5. Therefore the system is

consistent at λ = 5.

[**3.9**](#br161)[** ](#br161)Answer:

The system has the unique solution at λ = 0. For such values of λ the solution of

the system has the form x = −1, x = λ−1, x = λ−1 − 4.

1

2

3

[**3.10**](#br162)[** ](#br162)Solution.

Since the matrix A has the size 3 × 3, and the matrix B has the size 2 × 2, then

the unknown matrix X can be represented in the form:

⎡

⎤

a b

⎢

⎥

X = c d

e f

⎢

⎥

,

where

a, b, c, d, e, f .

are some real numbers

⎣

⎦

Having substituted this matrix into the equation A·X·B = C, we obtain a system

of linear equations relative to the unknowns a, b, . . . , f :

⎧

⎪ 3 + 3 − 2 − 2 − 3 − 3 = −13

⎪

a

b

c

d

e

f

,

⎨

2a + 2b − c − d − 4e − 4f = −25,

−6a − 6b − c − d − 2e − 2f = −33.

⎪

⎪

⎩





164

3 Systems of Linear Equations

Bring the augmented system matrix to the echelon form:

⎡

⎤

3

2

3 −2 −2 −3 −3 | −13

2 −1 −1 −4 −4 | −25

⎢

⎥

M =

⎢

⎥ →

⎣

⎦

−6 −6 −1 −1 −2 −2 | −33

⎡

⎤

3 3 −2 −2 −3 −3 | −13

⎢

⎥

→ ⎢0 0 1 1 −6 −6 | −49⎥ .

⎣

⎦

0 0 0

0

1

1 |

8

As the basic minor we select, for example, M1,2,3 = 0. Hence, b, d, f are the

1,3,5

independent variables by which the variables a, c, e are expressed:

⎡

⎤

3 − b b

⎢

⎥

X = −1 − d d

⎢

⎥

,

where

b, d, f

∈ R

.

⎣

⎦

8 − f f

[**3.11**](#br162)[** ](#br162)Answer:

⎡

⎤

a

b

(1) X = ⎣

⎦ , where a, b ∈ R;

−2 − 3a 2 − 3b

(2) X ∈ ∅, i.e. there are no solutions;

⎡

⎤

5a 3(a − 1) −a − 4

1 ⎢

⎥

(3) X = ⎢5 3 − 5

⎥ , where a, d, g ∈ R;

d

d

−

d

⎣

⎦

5

5g 3(g + 1) 4 − g

(4) X ∈ ∅.

[**3.12**](#br162)[** ](#br162)Solution.

Denote the initial values of the elements of the array a[] by a[1], a[2], ...,

a[5]. After executing the program segment code, the array a[] will contain the

following elements:

16a[1]+16a[5],

-8a[1]+16a[2]-8a[5],

4a[1]-8a[2]+16a[3]+4a[5],

-2a[1]+4a[2]-8a[3]+16a[4]-2a[5],

a[1]-2a[2]+4a[3]-8a[4]+17a[5].





Answers and Solutions

165

We obtain system of linear equations with ﬁve unknowns. Its solution is a[1] =

−4, a[1] = 1, a[1] = 3, a[1] = 3, a[1] = 2. Hence, the initial array has the form

[−4, 1, 3, 3, 2].

[**3.13**](#br162)[** ](#br162)Answer: [−14, −5, −2, 1, 1, 1, 5].

[**3.14**](#br163)[** ](#br163)Solution.

import math

def gauss\_jordan\_elimination(A, B):

m = len(A)

n = len(A[0])

if len(B) != m:

raise ValueError

C = [[A[i][j] if j != n else B[i]

for j in range(n+1)] for i in range(m)]

for r in range(n):

max\_row\_pos = r

\# Pivoting strategy

for i in range(r + 1, n):

if abs(C[i][r]) > abs(C[max\_row\_pos][r]):

max\_row\_pos = i

C[r], C[max\_row\_pos] = C[max\_row\_pos], C[r]

if math.isclose(C[r][r], 0):

continue

for i in range(n):

factor = C[i][r] / C[r][r]

for j in range(n + 1):

if i != r and j != r:

C[i][j] -= factor

C[r][j]

\*

for i in range(n):

if i != r:

C[i][r] = 0.0

for j in range(n + 1):





166

3 Systems of Linear Equations

if j != r:

C[r][j] /= C[r][r]

C[r][r] = 1.0

answer = [0]

n

\*

for i in range(n):

if not math.isclose(C[i][i], 0):

answer[i] = C[i][n] / C[i][i]

elif not math.isclose(C[i][n], 0):

return None

return answer

Let us give an example of a call of the function gauss\_jordan\_

elimination():

size = 100

A = [[0 for j in range(size)]

for i in range(size)]

B = [0 for i in range(size)]

for i in range(size):

for j in range(size):

A[i][j] = 1 if j == i else 0

for i in range(size):

B[i] = float(i)

print(A)

print(B)

print(gauss\_jordan\_elimination(A, B))

The asymptotic complexity of the Gauss–Jordan method coincides with the

complexity of Gaussian method and is e[qual](#br422)[ ](#br422)[to](#br422)[ ](#br422)O(n3), where n is the number of

equations of the initial system of equations [[58](#br422)[\].](#br422)





Answers and Solutions

167

[**3.15**](#br163)[** ](#br163)Solution.

(1) Denote the system matrix by A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

⎡

⎤

1 −4 1

⎣

1 −4 1

0 5 −2

0 10 −4

1 −4 1

⎢

⎥

(2)−(1) ⎢

⎥

⎢

⎥

A = 1 1 −1

⎢

⎥ → (3)−3(1) ⎢

⎥ → (3)−2(2) ⎢

0 5 −2

⎥

.

⎦

⎣

⎦

⎣

⎦

3 −2 −1

0 0

0

The rank of the matrix is equal to two, and the number of variables is equal to

three. This implies that the system will have 3 − 2 = 1 free variables.

Write the resulting equations:

⎧

⎨

x1 − 4x2 + x3 = 0,

5x − 2x = 0.

⎩

2

3

As the independent variable, select x :

3

⎧

3

⎪

⎨x = x ,

1

3

5

2

⎪

⎩

x2 = x3.

5

As a result we obtain the fundamental system of solutions: {[3, 2, 5]T }.

(2) Write the system matrix A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

2 −1 3 1

2 −1 3

1

⎢

⎥

(2)−(1) ⎢

⎥

A = 2 −5 −1 0

⎢

⎥ → (3)−2(1) ⎢

0 −4 −4 −1

⎥ →−1(2)

⎣

⎦

⎣

⎦

⎤

4 −7 1 3

0 −5 −5 1

⎡

⎤

⎡

2 −1 3 1

2 −1 3 1

0 4 4 1

0 0 0 9

⎢

⎥

⎢

⎥

→ ⎢0 4 4 1⎥ →

4(3)+5(2) ⎢

⎥

.

⎣

⎦

⎣

⎦

0 −5 −5 1

It is clear that the rank of the matrix is rk A = 3, the number of variables is

equal to 4. Therefore, the system will have 4 − 3 = 1 free variables. Write the

resulting equations:

⎧

⎪ 2

−

\+ 3x3

\+

= 0

⎪ x1 x2

x4

,

⎨

4x + 4x + x = 0,

2

3

4

⎪

⎪

⎩

9x4 = 0.





168

3 Systems of Linear Equations

As the independent variable, select x3:

⎧

⎪

= −2x3,

x2 = −x3,

x4 = 0.

⎪x1

⎨

⎪

⎪

⎩

The fundamental system of solutions is {[−2, −1, 1, 0]T }.

(3) Write the system matrix A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

1 2 4 −3

3 5 6 −4

1 2

4

−3

5

⎢

⎥

4 − 2 ⎢

( ) ( )

⎥

⎢

⎥

⎢

⎥

(2)−3(1) 0 −1 −6

⎢

⎥

⎢

⎥

A = ⎢

⎥ → (

3)−4(1)

⎢

⎥ .

⎢

⎥

⎢

⎥

4 5 −2

3 8 24 −19

3

0 −3 −18 15

0 3 18 −15

⎣

⎦

⎣

⎦

Note that the second, third and the fourth rows are proportional:

⎡

⎤

1 2 4 −3

0 −1 −6 5

A →

⎣

⎦

.

The rank of the matrix rk A = 2, the number of variables is 4. Therefore, the

system will have 4 − 2 = 2 free variables. Write the resulting equations:

⎧

⎨

x1 + 2x2 + 4x3 − 3x4 = 0,

−x − 6x + 5x = 0.

⎩

2

3

4

As the independent variables, select x and x :

3

4

⎧

⎨

x1 = 8x3 − 7x4,

⎩

x2 = −6x3 + 5x4.

The fundamental system of solutions is {[8, −6, 1, 0]T , [−7, 5, 0, 1]T }.

(4) Write the system matrix A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

⎡

⎤

3 5 2

4 7 5

1 1 −4

2 9 6

1 1 −4

4 7 5

3 5 2

2 9 6

1 1 −4

⎢

⎥

⎢

⎥

2 −4 1 ⎢

⎥

( ) ( )

⎢

⎥

⎢

⎥

⎢

⎥

(3)−3(1) 0 3 21

⎢

⎥

⎢

⎥

⎢

⎥

(1)↔(3)

→ (4)−(3)

A = ⎢

⎥ →

→ 4 −2 1

( ) ( ) ⎢

⎢

⎥

⎥

⎢

⎥

⎢

⎥

⎢

0 2 14

0 7 14

⎥

⎣

⎦

⎣

⎦

⎣

⎦





Answers and Solutions

169

⎡

⎤

⎡

⎤

1 1 −4

0 3 21

0 2 14

0 5 0

1 1 −4

0 3 21

0 0 0

0 5 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

3(3)−2(2)

→

→

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎣

⎦

⎣

⎦

The third row entirely consists of zero elements and can be eliminated from the

system matrix.

⎡

⎤

⎡

⎤

⎡

⎤

1 1 −4

0 3 21

0 5 0

1 1 −4

0 5 0

0 3 21

1 1 −4

0 5 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ →(2)↔(3) ⎢

⎥ → 5(3)−3(2) ⎢

⎥

.

⎣

⎦

⎣

⎦

⎣

⎦

0 0 105

The rank of the matrix rk A = 3, the number of variables is 3. Therefore, the

system has no free variables. Write the resulting equations:

⎧

⎪

\+

− 4x3 = 0

⎪x1 x2

,

⎨

5x2 = 0,

⎪

⎪

⎩

105x3 = 0.

Therefore

⎧

⎪

= 0

x2 = 0,

x3 = 0.

⎪ x1

,

⎨

⎪

⎪

⎩

As a result, the system has only the trivial solution: [0, 0, 0]T .

(5) Write the system matrix and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

⎡

⎤

2 4 6 1

1 2 3 1

3 6 9 −1

1 2 3 5

1 2 3 0

1 2 3 1

3 6 9 −1

1 2 3 5

1 2 3 0

⎢

⎥

⎢

⎥

(2)−(1) ⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

(3)−3(1) 0 0 0 1

⎢

⎥

⎢

⎥

⎢

⎥

(1)−(2)

A = ⎢

⎥ →

→

( ) ( ) ⎢

4 − 1

⎢

⎥

⎥ .

⎢

⎥

⎢

⎥

⎢

⎥

0 0 0 −1

⎣

⎦

⎣

⎦

⎣

⎦

0 0 0 5

The second, third and fourth rows are proportional:

⎡

⎤

⎦

1 2 3 0

0 0 0 1

A →

⎣

.





170

3 Systems of Linear Equations

The rank of the matrix rk A = 2, the number of variables is equal to four,

therefore, the system will have 4 − 2 = 2 free variables. Write the resulting

equations:

⎧

⎨

x1 + 2x2 + 3x3 = 0,

x4 = 0.

⎩

Therefore

⎧

⎨

x1 = −2x2 − 3x3,

x4 = 0.

⎩

The fundamental system of solutions is {[−2, 1, 0, 0]T , [−3, 0, 1, 0]T }.

(6) Write the matrix A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

1 2 3

1 2

3

⎢

⎥

(2)−2(1) ⎢

⎥

A = 2 3 4

⎢

⎥ → (3)−(1) ⎢

0 −1 −2

0 −1 −2

⎥

.

⎣

⎦

⎣

⎦

1 1 1

The second and the third rows are proportional:

⎡

⎤

1 2

3

A →

⎣

⎦

.

0 −1 −2

The rank of the matrix rk A = 2, the number of variables is equal to three.

Therefore, the system will have 3 − 2 = 1 free variables. Write the resulting

equations:

⎧

⎨

x + 2y + 3z = 0,

−y − 2z = 0.

⎩

Therefore

⎧

⎨

x = z,

⎩

y = −2z.

The fundamental system of solutions is {[1, −2, 1]T }.





Answers and Solutions

171

(7) Write the system matrix A and bring it to the upper triangular form.

⎡

⎤

⎡

⎤

1 −2 3 −4

⎢

1 −2 3 −4

⎢

⎥

(2)−2(1) ⎢

⎥

⎢

⎥

⎢

⎥

2 −4 5

7

(3)−6(1) 0 0 −1 15

⎥

⎢

⎥

→ (4)−7(1)

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

6 −12 17 −9

0 0 −1 15

0 0 −2 45

⎣

⎦

⎣

⎦

⎤

7 −14 19 17

The second and the third rows are proportional:

⎡

⎤

⎡

1 −2 3 −4

0 0 −1 15

0 0 −2 45

1 −2 3 −4

0 0 −1 15

0 0 0 15

⎢

⎥

⎢

⎥

⎢

⎥ → (3)−2(2) ⎢

⎥

.

⎣

⎦

⎣

⎦

The rank of the matrix rk A = 3, the number of variables is equal to four.

Therefore, the system will have 4 − 3 = 1 free variables. Write the resulting

equations:

⎧

⎪

− 2x2 + 3x3 − 4x4 = 0

⎪x1

,

⎨

−x + 15x = 0,

3

4

⎪

⎪

⎩

15x4 = 0.

Therefore

⎧

⎪

= 2x2,

⎪x1

⎨

x3 = 0,

x4 = 0.

⎪

⎪

⎩

The fundamental system of solutions has the form {[2, 1, 0, 0]T }.





**Chapter 4**

**Complex Numbers and Matrices**

As was already mentioned in Chap. [1](#br16), complex numbers may appear as matrix

elements. Moreover, the characteristics of real matrices (such as eigenvalues, see

Chap. [5](#br228)[ ](#br228)“Vector Spaces” on page [226](#br237)) in some cases appear to be complex. In this

connection, let us discuss the methods of algebra of complex numbers.

**Complex number** z is an ordered pair of real numbers (a, b), where a, b ∈ R.

The ﬁrst number a is called the **real part** of the complex number z = (a, b) and

is denoted by symbol Re z, while the s[econd](#br421)[ ](#br421)number of the pair b is called the

**imaginary part** z and is denoted by Im z [[24](#br421)[\].](#br421)

A complex number of the form (a, 0), where the imaginary part is zero, is

identiﬁed with the real number a, i.e. (a, 0) ≡ a. This allows considering the set of

all real numbers R as a subset of a set of complex numbers C.

Two complex numbers z = (a , b ) and z = (a , b ) are considered equal if

1

1

1

2

2

2

and only if their real and imaginary parts are pairwise equal: z = z ⇔ a = a ,

1

2

1

2

b1 = b2.

**4.1 Arithmetic Operations with Complex Numbers**

On the set C are deﬁned the operations of addition and multiplication of complex

numbers. **Sum** of complex numbers z = (a , b ) and z = (a , b ) is the complex

1

1

1

2

2

2

number z, equal to z +z = (a + a , b + b ). **Product** of numbers z = (a , b )

1

2

1

2

1

2

1

1

1

and z = (a , b ) is such a complex number z = (a, b), that a = a a − b b ,

2

2

2

1

2

1 2

b = a1b2 + a2b1.

The pair (0, 1) is of the greatest importance in the operations with complex

numbers; it is denoted by (0, 1) ≡ i and is called **imaginary unit**. The basic

property of the imaginary unit consists in that i2 = i · i = (0, 1) · (0, 1) = (−1, 0),

or i2 = −1.

© Springer Nature Switzerland AG 2021

173

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_4>





174

4 Complex Numbers and Matrices

A complex number of the form z = (0, b) is called **purely imaginary**. Since

(0, b) = (b, 0) · (0, 1), then the purely imaginary number z is presentable in the

form of the product z = bi.

Any complex number can be presented in the form

z = (a, b) = (a, 0) + (0, b) = (a, 0) + (b, 0) · (0, 1) = a + ib.

Such a notation is referred to as the **algebraic form** of a complex number. This

allows considering i as a factor, whose square is equal to −1, and performing oper-

ations with complex numbers in the same manner as with algebraic polynomials, in

intermediate calculations assuming i2 = −1.

Example 4.1 Let z = 2 + 5i, z = −3 + 2i. Then, the addition of these numbers

1

2

will result in a complex number

z1 + z2 = (2 + 5i) + (−3 + 2i) = (2 − 3) + (5 + 2)i = −1 + 7i.

(4.1)

The product of the numbers z and z is computed by multiplying the expressions

1

2

(2 + 5i) and (−3 + 2i) as polynomials with regard to the equality i

2 = −1:

z1z2 = (2 + 5i)(−3 + 2i) = 2(−3) + 2(2i) − 3(5i) + (5i)(2i)

= −6 + 4i − 15i + 10i2 = −6 − 10 + (4 − 15)i = −16 − 11i.

(4.2)

A complex number z∗ = (a, −b) = a − ib is called a **conjugate** of the complex

number z = (a, b) = a+ib. There is one more frequent notation of a conjugate—z.

If the coefﬁcients of the polynomial p(z) are real, the equality (p(z))∗ = p(z∗) is

valid.

It is convenient to present the number z = a + ib as the point (x, y) of a plane

with Cartesian coordinates x = a and y = b. Correlate each complex number z

with a point with coordinates (x, y) (and a position vector, connecting the origin

of coordinates with this point). Such a plane is denoted by  and is referred to

z

as **complex plane** (see Fig. [4.1](#br187)). Note that [geomet](#br186)ric interpretation of complex

numbers is sometimes referred to as the **Argan[d**](#br186)[**1](#br186)[ ](#br186)diagram**.

Many applications widely use a **trigonometric form** of the complex number z.

Let us introduce the polar coordinate system so that the pole is at the origin of

Cartesian system (x, y). The axis of the polar system will be directed along the

positive direction of the axis Ox.

1Jean-Robert Argand (1768–1822), French mathematician.





4.1 Arithmetic Operations with Complex Numbers

175

**Fig. 4.1** Representation of

the number z on a complex

plane

y

z = a+ ib

b = Im z

ρ

ϕ

O

a = Re z

x

In this case, Cartesian and polar coordinates of an arbitrary point other than the

origin of coordinates are related by the formulae

x = ρ cos ϕ, y = ρ sin ϕ,

⎧

y

⎪arctan

if

if

0;

⎪

,

x >

⎪

⎪

x

y

⎪

⎪

⎪

⎪

⎪arctan

\+

x < , y

0

` `0;

\+

⎨

π,

x

y

ρ = x2 + y ,

2

ϕ

\=

⎪

⎪

⎪arctan − π, if x < 0, y < 0;

⎪

⎪

⎪

x

⎪

⎪

⎪π

⎩

sign y,

if x = 0.

2

As a result, we obtain a trigonometric form of the number z

z = (x, y) = x + iy = ρ(cos ϕ + i sin ϕ).

The value ρ is called **modulus**, and ϕ—**argument** of the complex number z and

denoted ρ = |z|, ϕ = arg z. It should be noted that the argument ϕ is ambiguously

determined: instead of the value ϕ we can take the value ϕ + 2πk, where k ∈ Z. If

argz is chosen in such a way that −π < argz  π, then such a value is called the

**principal** value of the argument.

For the numbers z1 = ρ (cos ϕ + i sin ϕ ) and z = ρ (cos ϕ + i sin ϕ ),

1

1

1

2

2

2

2

speciﬁed in the trigonometric form,

z1z2 = ρ1ρ2(cos(ϕ1 + ϕ2) + i sin(ϕ1 + ϕ2)),

z1

z2

ρ1

ρ2

\=

(cos(ϕ − ϕ ) + i sin(ϕ − ϕ )), ρ = 0.

1

2

1

2

2





176

4

Complex Numbers and Matrices

y

y

z z

1

2

z1 + z2

z1

z2

z2

z1

ϕ1 + ϕ2

ϕ2

ϕ1

O

x

O

x

**Fig. 4.2** Sum is the panel (**a**), and product is the panel (**b**) complex numbers z1 and z2

Geometric illustration of the sum and the product of complex numbers is shown

in Fig. [4.2](#br188). For any z , z ∈ C, the position vector of the sum z + z is equal to

1

2

1

2

the sum of the position vectors of the summands z and z . The position vector of

1

2

the product z z is obtained by rotating the position vector of the number z by the

1

2

1

angle of a[rg](#br188)[ ](#br188)z counter-clockwise and extending by |z | times.

2

2

**Euler’[s**](#br188)[**2](#br188)[ ](#br188)formula** relates the exponential function of the imaginary argument

with trigonometric functions of the imaginary part of the argument:

eiϕ = cos

ϕ

\+ sin

i

ϕ.

This is why we can introduce one more notation of the complex number, namely,

**exponential**: z = ρeiϕ. The exponential notation is convenient for operations of

multiplication, division, raising to a power and extraction of root. For example, the

n-th power of the number z can be presented in the form

zn = (ρe )

iϕ n =

n

ρ e

ρ (

inϕ = n cos

nϕ

\+ sin

i

nϕ)

for all integer values n.

An important consequence of the obtained formula

(cos ϕ + i sin ϕ)n = cos nϕ

i

\+ sin

nϕ

is associated with the name of **de Moivre**.[3](#br188)

The n-th root of z = ρ(cos ϕ + i sin ϕ) can be calculated as

√

1/n

= [ρ(cos(ϕ + 2πk) + i sin(ϕ + 2πk))]1/n

n z ≡ z

,

k ∈ Z,

2Leonhard Euler (1707–1783), prominent Swiss mathematician.

3Abraham de Moivre (1667–1754), English mathematician of French origin.





4.1 Arithmetic Operations with Complex Numbers

177

or, after applying Euler’s formula,

$

$

%

$

%%

√

\+ 2

n

\+ 2

n

ϕ

πk

ϕ

πk

1/n

n z = ρ

cos

\+ i sin

,

k = 0, 1, . . . , n − 1.

Here we obtain n possible values of the n-th root for k = 0, 1, . . . , n − 1. Other

√

acceptable k do not result in new values of z. For example, for k = n the argument

n

is argz = ϕ/n + 2π and differs from the case k = 0 by 2π, which corresponds to

the complex number equal to it.

Example 4.2 Denote roots of the equation zn = 1, where n is a natural number, by

ω , k = 0, . . . , n − 1. Prove that on a complex plane the points corresponding to

k

the values ω are located at the vertices of a regular n[-gon,](#br421)[ ](#br421)inscribed in a unit circle,

k

whose centre is located at the origin of coordinates [[24](#br421)[\].](#br421)

**Proof** According to the introduced deﬁnition,

2πi k/n

= e2πik/n

ωk = (e

)

,

k = 0, 1, . . . , n − 1.

(4.3)

(4.4)

(4.5)

√

In particular, for n = 4 we have the following values 4 1:

2πi k/4

= eπik/2

ωk = (e

)

,

k ∈ {0, 1, 2, 3},

or, after computing the complex exponents:

ωk = 1, i, −1, −i.

Modulus of the complex number ω = e2πik/n is equal to one for all values of

k

the variable k, and the argument is equal to argω = 2πk/n, k = 0, 1, . . . , n − 1.

k

Thereby, we can conclude that the n-th roots of one are located on the unit circle

C, and the ﬁrst root ω0, associated with k = 0, lies in the real axis, and ω divide

k

the circle by n arcs of the same length (see the example for the instance n = 9 in

Fig. [4.3](#br189)).

**Fig. 4.3** Location of the

roots of the n-th power of one

on the unit circle for n = 9

y

C

O

1

x





178

4 Complex Numbers and Matrices

**4.2 Fundamental Theorem of Algebra**

**Theorem 4.1 (Fundamental Theorem of Algebra)** States that [any](#br421)[ ](#br421)polynomial of

a non-zero degree with complex coefﬁcients has a complex root [[43](#br421)[\]](#br421). This is why

an arbitrary polynomial with real (or complex) coefﬁcients always has some root

z ∈ C.

Each polynomial of degree n

p(z) = cnzn +

cn−1zn−1 + · · · +

c0, ci

∈ C for = 0 1 = 0

, , . . . , n, c

i

,

n

can uniquely (accurate to the order of cofactors) be expanded into the product

p(z) = cn(z − z1)m1 (z z2)m2 . . . (z z )mk ,

−

−

k

where z is a root of the polynomial p(z) with a multiplicity of m , 1  i  k.

i

i

For polynomials with degree lower than the ﬁfth, we can always ﬁnd the roots

having expressed them by arithmetic operations or arithmetic roots of an arbi-

trary multiplicity, or **radicals**. The [met](#br190)hod for calculating the cubic polynomial’s

roots was suggested [by](#br190)[ ](#br190)**Carda[nus**](#br190)[**4](#br190)[ ](#br190)**(see Sect. [4.3](#br190)[ ](#br190)below), of the fourth degree

polynomial—**Ferrari**.[5](#br190)[ ](#br190)However, there are no common methods for ﬁnding roots

of polynomials of higher degrees, according to next theorem:

**Theorem 4.2 (Abel[**6](#br190)–Ruf[ﬁni**](#br190)[**7](#br190)[ ](#br190)Theorem)** Any arbitrary equation of degree n for

n  5 is unsolvable in radicals.

**4.3 Cardano Formula**

In order to determine the roots of the cubic equation

3

2

az + bz + cz + d = 0, where a, b, c, d ∈ C,

(4.6)

b

proceed as follows. Using the change of the variable z = y −

brought to a **canonical form**

the equation is

3a

y3 + py + q = 0, p, q ∈ C.

(4.7)

4Hieronymus Cardanus (1501–1576), Italian mathematician and philosopher.

5Lodovico Ferrari (1522–1565), Italian mathematician.

6Niels Henrik Abel (1802–1829), Norwegian mathematician.

7Paolo Rufﬁni (1765–1822), Italian mathematician.





4.3 Cardano Formula

179

By **Cardano [form](#br421)ula**, the roots of the cubic equation y , y , y in the canonical

1

2

3

form are equal [[33](#br421)[\]](#br421)

y1 = α + β,

α + β

(4.8)

(4.9)

√

α − β

y2 = −

y3 = −

\+ i 3 ·

,

,

2

α + β

2

2

α − β

2

√

− i 3 ·

(4.10)

where

,

\-

\-

q

α =

3 −

\+

Q,

2

,

q

β =

3 −

−

\+

Q,

2

$ %

$ %

3

2

p

q

Q =

.

3

2

Using these relations, one should for each of the three values of the cube root of

α take that value of the root β, for which the equality αβ = −p/3 is valid.

Example 4.3 Find the roots of the equation z

formula.

3−5 2+9 −5 = 0, using the Cardano

z

z

5

**Solution** Replace the variable z = y + . We obtain the cubic equation in the

3

canonical form

2

20

y3 + y +

= 0,

27

(4.11)

3

2

20

27

here p = , q =

. Further using Cardano formula ([4.8](#br191))–([4.10](#br191)):

3

$

%

$ %

3

2

4

p

q

Q =

\+

\=

,

3

2

27

.

,

\+

√

3

10

27

4

1 3

3

α, β =

−

±

\=

−10 ± 6 3.

27

\- √

1

3

3

Let α =

6 3 − 10, then, in order for the condition αβ = −p/3 to be

\- √

1

3

3

satisﬁed, we choose β = −

6 3 + 10. The roots of the equation will have the





180

4

Complex Numbers and Matrices

form

\+

\+

√

√

1

3

3

3

y1 =

6 3 − 10 − 6 3 + 10 ;

√

\+

\+

\+

\+

√

√

√

√

√

√

y2 = −1

6 3 − 10 − 6 3 + 10

\+

−

3

6 3 − 10 + 6 3 + 10 ;

3

3

i

i

3

3

6

6

√

3

\+

\+

\+

\+

√

√

y3 = −1

6 3 − 10 − 6 3 + 10

6 3 − 10 + 6 3 + 10 .

3

3

3

3

6

6

√

The obtained expressions can be simpliﬁed, if we note that the equality 6 3 ±

√

\- √

√

3

3

10 = ( 3 ± 1) is valid. Then 6 3 ± 10 = 3 ± 1, and

$√

√

%

1

3

2

y1 =

3 − 1 − ( 3 + 1) = − ;

3

√

$√

√

%

$√

$√

√

%

%

y2 = −1

3 − 1 − ( 3 + 1) +

3

3 − 1 + 3 + 1 = + i;

1

i

i

6

6

3

√

$√

√

%

√

y3 = −1

3 − 1 − ( 3 + 1) −

3

3 − 1 + 3 + 1 = − i.

1

6

6

3

5

Returning to the original variable z = y + , we obtain z = 1, z = 2 + i,

1

2

3

z3 = 2 − i.

**4.4 Complex Coefﬁcient Matrices**

Among the complex coefﬁcient matrices, classes of Hermitian and unitary matrices

play a special role in algebra and its applications.

**4.4.1 Hermitian Matrices**

Consider the matrix Z, containing the complex elements Z = (z ), where i =

ij

1, 2, . . ., m, j = 1, 2, . . . , n. **Hermitian conjugate** matrix relative to Z is the

matrix ZH , whose elements are equal to

∗

z .

ji

z

H =

(4.12)

ij

In order to obtain Hermitian conjugate matrix, the operations of transposition and

complex conjugation are applied to the initial matrix. The mentioned operations are





4.4 Complex Coefﬁcient Matrices

181

independent and can be executed in any sequence.

⎡

⎤

1 + i 2 + 3i

−1 5 − 4i

Example 4.4 A Hermitian conjugate matrix relative to Z = ⎣

⎦ is the

matrix

⎛

⎞

⎡

⎤

∗

⎛⎡

⎤⎞∗

⎡

⎤

T

1 + i 2 + 3i

−1 5 − 4i

1 + i −1

2 + 3i 5 − 4i

1 − i −1

2 − 3i 5 + 4i

⎜

⎟

ZH =

⎣

⎦

= ⎝⎣

⎦⎠ = ⎣

⎦

.

⎝

⎠

(4.13)

Note Often, for designation of a Hermitian conjugate matrix, the notations Z† or

Z+ are used.

Let us enumerate the main properties of the Hermitian conjugation operation:

\1. IH = I;

\2. (Z + Z )H = ZH + ZH ;

1

2

1

2

\3. (λZ)H = λ∗ZH ∀λ ∈ C;

\4. (ZH )H = Z;




\5. if A−1 exists, then A−1

H

= AH −1;

\6. det AH = det A∗ = (det A)∗.

**Theorem 4.3** If for the complex matrices Z and Z the product Z Z is deter-

1

2

1 2

mined, then

(Z1Z2)H = Z Z .

H

H

(4.14)

2

1

**Proof** The validity of the theorem follows from the property of the matrix product

transposition (see Problem [**1.3**](#br39)):

(Z1Z2)T = Z Z .

T

T

(4.15)

2

1

With the help of Eq. ([4.15](#br193)) we obtain a chain of equalities

(Z1Z2)H = ((Z1Z2)T )∗ = (Z Z )

∗ =

∗

(Z ) (Z )

∗ =

Z Z ,

2 1

(4.16)

T

2

T

1

T

T

H

H

2

1

which proves the identity ([4.14](#br193)).

Among complex matrices, Hermitian matrices are very widely used. **Hermitian**

matrix is a square matrix, where ZH = Z. A respective condition for the elements

of such a matrix: ∀i, j (z = z∗ ). In other words, the Hermitian matrix coincides

ij

ji

with its Hermitian-conjugated.





182

4 Complex Numbers and Matrices

⎡

⎤

1

−3 − i

Example 4.5 The matrix Z = ⎣

⎦ is Hermitian, as is easy to see.

−3 + i

1

Let us verify it.

⎛

⎞

⎡

⎤

∗

⎛⎡

⎤⎞∗

⎡

⎤

T

1

−3 − i

1

−3 + i

1

−3 − i

⎜

⎟

ZH =

⎣

⎦

= ⎝⎣

⎦⎠ = ⎣

⎦

.

⎝

⎠

−3 + i

1

−3 − i

1

−3 + i

1

(4.17)

Recall that applying the complex conjugation operation to a real number does

not change this number.

Note Hermitian matrices are also referred to as **self-adj[oint**](#br421)[** ](#br421)**matrices. The theory of

self-adjoint matrices is widely used in modern physics [\[](#br421)[44](#br421)[\].](#br421)

**4.4.2 Unitary Matrices**

A square matrix U with complex elements is called **unitary**, of the condition

H

\=

I

is met. The condition of unitarity can be written in other equivalent

U U

forms as follows:

UUH =

I

or

UH = U−1

.

(4.18)

⎡

⎤

1

1 1

Example 4.6 Prove that the matrix Z = √ ⎣

⎦ is unitary. To do this, compute

2

−

i i

the product ZH Z:

⎛⎡

⎤⎞

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

H

1

1 1

1

1 1

1

1 i

1 −

1

1 1

1 0

0 1

H

Z Z

= √ ⎝⎣

⎦⎠ √ ⎣

⎦ = √ ⎣

⎦ √ ⎣

⎦ = ⎣

⎦

.

2

−

2

−

2

2

−

i i

i i

i

i i

(4.19)

Therefore, Z is a unitary matrix.

**Theorem 4.4** The determinant of a unitary matrix is a complex number whose

modulus is equal to one.

**Proof** See in Problem [**4.51**](#br212).

There is a close connection between unitary and Hermitian matrices: each un[itary](#br421)

matrix A is presented in the form A = exp(iB), where B is a Hermitian matrix [[26](#br421)[\].](#br421)





4.5 Fundamentals of Quantum Computing

183

**4.5 Fundamentals of Quantum Computing**

In quantum computers, for implementation of computing, processes of a quantum

nature are used manifested in experiments with objects of the microcosm—

elementary particles, atoms, molecules, molecular clusters, etc. The description

of such processes is based on the application of complex numbers and complex

matrices.

As is well known, the basic notion of classical information theory is **bit** [[18](#br420)[\].](#br420)[ ](#br420)A

classical bit takes the values 0 or 1 (and no other).

Qubit (quantum bit) is the sma[llest](#br420)[ ](#br420)[elem](#br422)ent that executes the information storage

function in a quantum computer [[6](#br420)[,](#br420)[ ](#br420)[54](#br422)[,](#br422)[ ](#br422)[75](#br422)[\].](#br422)

**Qubit** is a quantum system |ψ
` `that allows two [states:](#br195)[ ](#br195)|0
` `and |1
` `[[54](#br422)[\].](#br422)[ ](#br422)In

[8](#br195)

accordance with the so-called bra-ket (bracket) Dirac notation, the symbols |0

or |1
` `are read as “ket 0” and “ket 1”, respectively. The brackets |. . .
` `show that ψ

is some state of the quantum system.

The fundamental difference between the classical bit and the qubit consists in

that the qubit can be in a state different from |0
` `or |1
. The arbitrary state of the

qubit is deﬁned by the linear combination of basic states:

|ψ
` `= u |0
` `+ v |1
` `,

(4.20)

where the complex coefﬁcients u and v satisfy the following condition:

2

2

|u| + |v| = 1.

(4.21)

The mathematical description of the basic states reduces to their representation

in matrix form:

⎡ ⎤

⎡ ⎤

1

0

|0
` `= ⎣ ⎦ , |1
` `= ⎣ ⎦ .

(4.22)

0

1

Based on the presentation ([4.22](#br195)) the arbitrary state of the qubit is written as

⎡ ⎤

u

|ψ
` `= ⎣ ⎦ .

(4.23)

v

8Paul Adrien Maurice Dirac (1902–1984), English physicist.





184

4 Complex Numbers and Matrices

A system of two qubits is set by a linear combination of basic states

⎡ ⎤

⎡ ⎤

⎡ ⎤

⎡ ⎤

1

0

0

0

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

0

1

0

0

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

|00
` `=

,

|01
` `=

,

|10
` `=

,

|11
` `=

.

(4.24)

(4.25)

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

0

0

1

0

⎣ ⎦

⎣ ⎦

⎣ ⎦

⎣ ⎦

0

0

0

1

Similarly are introduced the states

|00 . . .00
` `, |00 . . .01
` `, . . . , |11 . . .11

of several interacting qubits. Such quantum states are called **computational basis**

**states** or, for short, **basis states**.

For changing the state of a quantum system, quantum operations are used referred

to as **gates** (quantum gate). Thus, the gates perform logical operations with qubits.

Note that the change of the state |ψ
` `in time is also referred to as the **evolution** of

the quantum system.

An important step of quantum algorithms is the procedure of **measurement of**

**state**. When the qubit state is measured, it randomly passes to one of its states: [|](#br195)0

or |1
. Therefore, the complex coefﬁcients u and v from the qubit deﬁnition ([4.20](#br195))

are associated with probability to get the value 0 or 1 when its state is measured.

According to the postulates of quantum theory, the probabilities of passing to the

states |0
` `and |1
` `are equal to |u|2 and |v|2, respectively. In this connection, the

equality ([4.21](#br195)) reﬂects the probability conservation law. After the measurement, the

qubit passes to the basic state, complying with the classical result of measurement.

Generally speaking, the probabilities of getting the result 0 and 1 are different for

different states of the quantum system.

In other words, the quantum computing is a sequence of simple form operations

with the collection of the interacting qubits. In the ﬁnal step of the quantum

computing procedure, the state of the quantum system is measured and a conclusion

about the computing result is made. The measurement makes it possible to obtain,

at a macroscopic level, the information about the quantum state. The peculiarity of

the quantum measurements is their irreversibility, which radically differentiates the

quantum computing from the classical one.

A quantum system, formed by N two-level elements, has (N) = 2N

independent states. The key point of functioning of such a system is the interaction

of separate qubits with each other. The number of states (N) grows exponentially

with the growth of the quantum system, which allows solving practical problems of a

very high asymptotic complexity (see section “Estimation of Algorithm Efﬁciency”

on page [13](#br28)). For example, an efﬁcient quantum algorithm of prime factorization

is known, which is very important for cryptography. As a result, the quantum

algorithms provide exponential or polynomial acceleration in comparison with the

classical solution methods for many problems.





4.5 Fundamentals of Quantum Computing

185

Unfortunately, no full-function quantum computer has been created yet, although

many of its [elements](#br422)[ ](#br422)have already been built and studied at the leading world’s

laboratories [[72](#br422)[\].](#br422)[ ](#br422)The main obstacle to the development of quantum computing

is instability of a system of many qubits. The more qubits are united into an

entangled system, the more effort is required to ensure smallness of the number of

measurement errors. Nevertheless, the history of quantum computer development

demonstrates an enormous potential laid in the uniting of quantum theory and

algorithm theory.

Prior to proceeding to des[cribing](#br197)[ ](#br197)the basic quantum operations with qubits, let

us introduce the notion of the Paul[i](#br197)[9](#br197)[ ](#br197)matrices and the Dirac matrices.

**4.5.1 Pauli Matrices and Dirac Matrices**

The matrices σ , σ and σ

1

2

3

⎡

⎤

⎡

⎤

⎦

⎡

⎤

⎦

0 1

0 −i

i 0

1 0

σ1 =

⎣

⎦

,

σ2

= ⎣

,

σ3

= ⎣

(4.26)

1 0

0 −1

are called the **Pauli matrices**. They are widely used in quantum theory for

describing half-integer spin particles, for example, an electron. [(Spi](#br421)n is a quantum

property of an elementary particle, intrinsic angular momentum [\[](#br421)[44](#br421)[\].](#br421)[ ](#br421)So, electrons,

protons and neutrino have half-integer spin; spin of photons and gravitons is

integer).

The following properties are valid for the Pauli matrices.

\1. The Pauli matrices are Hermitian and unitary:

∀k ∈ {1, 2, 3} σ = σH = σ−1.

(4.27)

k

k

k

\2. ∀k ∈ {1, 2, 3} the square of the Pauli matrix is equal to the identity matrix:

⎡

⎤

1 0

0 1

2

i

⎣

⎦

σ =

.

(4.28)

(4.29)

\3. ∀i, j ∈ {1, 2, 3} the equalities are valid

⎡

⎣

⎤

⎦

1 0

0 1

σ σ + σ σ = 2δ

.

i

j

j

i

ij

9Wolfgang Ernst Pauli (1900–1958), Swiss and American physicist.





186

4 Complex Numbers and Matrices

Sometimes, in linear algebra [an](#br421)[d](#br421)[ ](#br421)[its](#br421)[ ](#br421)applications, one has to use matrices split

into rectangular parts or blocks [[25](#br421)[,](#br421)[ ](#br421)[47](#br421)[\].](#br421)[ ](#br421)Consider the rectangular matrix A = (a ),

ij

where 1  i  m, 1  j  n. Let m = m + m , n = n + n .

1

2

1

2

Let us draw horizontal and vertical lines and split the matrix A into four

rectangular blocks:

n1

n2

B11

B21

B12

B22

m1

m2

A =

(4.30)

Thus, the matrix A is presented in the form of a **block matrix**, consisting of the

blocks B , B , B , B of size m ×n , m ×n , m ×n , m ×n , respectively.

11

12

21

22

1

1

1

2

2

1

2

2

As an example of block matrix setting, we provide the deﬁnition of the Dirac

matr[ices.](#br420)[ ](#br420)Four **Dirac matrices** α , α , α , β are part of the equation named after

1

2

3

him [[4](#br420)[\]](#br420), for a half-integer spin relativistic particle, and are expressed in terms of the

Pauli matrix σk, k = 1, 2, 3, as follows:

⎡

⎤

⎡

⎤

O σ

I O

⎣

k⎦

= ⎣

⎦

(4.31)

αk =

,

β

,

σ O

k

O −I

where O is a non-zero matrix of size 2 × 2, I is an identity matrix of the same size.

(Relativistic are the particles whose velocity is close to the light velocity.)

Each of the Dirac matrices has a Hermitian property and a unitary property.

Moreover, for all l, m ∈ {1, 2, 3} the equalities are valid:

α α + α α = 2δlmI,

(4.32)

(4.33)

l

m

m l

α β + βα = O.

l

l

Note that the size of the matrices I and O in formulae ([4.32](#br198)) and ([4.33](#br198)) is equal to

4 × 4.

**4.5.2 Basic Operations with Qubits**

Consider the basic operations with qubits.

The inﬂuence of a quantum gate on the qubit |ψ
` `[is](#br422)[ ](#br422)[ex](#br422)erted by applying a

**quantum-mechanical operator**, for example, U |ψ
` `[[67](#br422)[,](#br422)[ ](#br422)[72](#br422)[\].](#br422)[ ](#br422)The operators may





4.5 Fundamentals of Quantum Computing

187

be presented in the form of unitary matrices. In particular, the evolution of a single

qubit is described by a unitary matrix of size 2 × 2.

Successive application of the series of operators U , U , ..., U to one qubit

1

2

n

is equivalent to the inﬂ[uence](#br422)[ ](#br422)of the operator W, whose matrix is a product of the

matrices U U . . . U [[54](#br422)[\]:](#br422)

1

2

n

U (U −1(. . . (U2(U1 |ψ
)) . . . )) = (U1U2 . . . U ) |ψ
` `= W |ψ
` `.

(4.34)

n

n

n

Such operator W is called a **composition** of operators U , U ,..., U . As a

1

2

n

consequence of non-commutativity of the matrix multiplication operation in the

general case the sequence of applying the quantum gates is of importance.

Example 4.7 Let us show that the application of the operator σ3 (see deﬁni-

tion ([4.26](#br197))) to the qubit in the state |ψ
` `= u |0
` `+ v |1
` `transfers it to the state

|ψ
` `= u |0
` `− v |1
.

**Proof** Write the qubit |ψ
` `in matrix representation:

⎡ ⎤

u

|ψ
` `= ⎣ ⎦ .

(4.35)

v

Deﬁne the action of σ3 on this quantum state:

⎡ ⎤

⎡

⎤ ⎡ ⎤

⎡

⎣

⎤

⎦

⎡ ⎤

⎡ ⎤

u

1 0

u

u

1

0

|ψ
` `= σ3

⎣ ⎦

\=

⎣

⎦ ⎣ ⎦

\=

= u

⎣ ⎦

− v

⎣ ⎦

= u |0
` `− v |1
` `.

v

0 −1

v

−v

0

1

(4.36)

Graphic representation of quantum operations in the form schemes or diagrams

(quantum circuit) is widely used.

Some quantum-mechanical operator U that transforms a single qubit (one qubit

gate) is represented as follows:

|ψin

|ψout

U

The sequence of steps of quantum algorithms corresponds to the direction on the

diagram from left to right.

In Table [4.1](#br200)[ ](#br200)the gates are enumerated that transform one qubit, and the matrix

representations of these gates.

Let us show the method of computing a quantum operation matrix based on its

action on the basic vectors.





188

4

Complex Numbers and Matrices

Matrix

**Table 4.1** One qubit operations

Name

Designation

/

0

1 0

Identity transformation

Pauli element X

Pauli element Y

I =

I

0 1

/

/

/

0

0 1

σ1 =

σ2 =

X

Y

1 0

0

0

0 −i

0

i

1

0

Pauli element Z

Hadamard element

Phase element

σ3 =

Z

H

S

0 −1

/

0

1 1

1

√

2

1 −1

/

0

1 0

0 i

/

0

1

0

Element π/8

T

0 eiπ/4

Measurement

Projection on |0
` `and |1

Hadamard[10](#br200)[ ](#br200)gate transforms the system’s state by the rule:

1

|0
` `→ √ (|0
` `+ |1
),

(4.37)

(4.38)

2

1

|1
` `→ √ (|0
` `− |1
).

2

Therefore, the arbitrary state |ψ
` `will in this case change as follows:

⎡ ⎤

⎡ ⎤

⎡ ⎤

u

1

0

|ψ
` `= ⎣ ⎦ = u ⎣ ⎦ + v ⎣ ⎦ →

v

0

1

⎡

⎤ ⎡ ⎤

1

1

1

1 1

u

→ u√ (|0
` `+ |1
) + v√ (|0
` `− |1
) = √ ⎣

⎦ ⎣ ⎦ .

(4.39)

2

2

2

1 −1

v

⎡

⎤

1

1 1

Thus, the Hadamard element is presented by the matrix √ ⎣

⎦.

2

1 −1

10Jacques Salomon Hadamard (1865–1963), French mathematician.





4.5 Fundamentals of Quantum Computing

189

**Table 4.2** Two qubits operations

Name

Designation

Matrix

⎡

⎤

⎥

1 0 0 0

0 0 1 0

⎢

⎢

⎥

Exchange

⎢

⎥

×

×

⎣0 1 0 0⎦

0 0 0 1

⎡

⎤

1 0 0 0

0 1 0 0

•

⎢

⎥

⎢

⎥

Controlled NOT

⎢

⎥

⎣0 0 0 1⎦

0 0 1 0

⎡

⎢

⎤

⎥

1 0 0 0

0 1 0 0

⎢

⎥

Controlled phase element

⎢

⎥

•

⎣0 0 1 0⎦

0 0 0 i

S

Obviously, in order to execute complex algorithms, the qubits must interact with

each other and exchange information. In this connection, of particular importance

are the logical operations that affect two or more qubits. In Table [4.2](#br201), the most

important gates are enumerated, that transform the state of two qubits.

Example 4.8 Let us determine how the qubit |ψ
` `is transformed under the action of

two applications of the Hadamard element:

|ψ

|

H

H

ψ

**Solution** As shown above, in matrix representation, the Hadamard element is

described by the matrix

⎡

⎤

1

1 1

MH = √

⎣

⎦

.

(4.40)

2

1 −1

Compute the matrix that corresponds to two applications of the Hadamard

element as a matrix product (see formula ([4.34](#br199))):

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

1

1 1

1

1 1

1

2

2 0

0 2

1 0

0 1

MH MH = √

⎣

⎦ · √ ⎣

⎦ =

⎣

⎦ = ⎣

⎦

.

(4.41)

2

1 −1

2

1 −1

An identity matrix is obtained, therefore, two applications of the Hadamard

element bring the qubit back to its original state.





190

4 Complex Numbers and Matrices

Example 4.9 Find a matrix representation of the following quantum circuit:

**Solution** The quantum circuit consists of two elements “controlled NOT”, also

referred to as “CNOT” (Controlled NOT).

The matrix of the element CNOT has the form (see Table [4.2](#br201)):

⎡

⎤

1 0 0 0

0 1 0 0

0 0 0 1

0 0 1 0

⎢

⎥

⎢

⎥

⎢

⎥

(4.42)

⎢

⎥

⎢

⎥

⎣

⎦

In view of the matrix representation of CNOT, compute how the arbitrary state

|ψ ψ 
` `= (u |0
` `+ v |1
)(u |0
` `+ v |1
) will change after the action of the ﬁrst

1

2

1

1

2

2

CNOT:

⎡

⎤

⎡

⎤ ⎡

⎤

⎡

⎤

u1

1 0 0 0

0 1 0 0

0 0 0 1

0 0 1 0

u1

u1

v

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎥

⎢

⎢

⎥

⎥

⎢v1⎥

⎢

⎥ ⎢ 1⎥ ⎢ 1⎥

v

|ψ ψ 
` `=

→

\=

.

(4.43)

⎢

⎥

⎢

⎥ ⎢

1

2

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

u2

v2

u2

v2

u2

⎣

⎦

⎣

⎦ ⎣

⎦

⎣

⎦

v2

This is equivalent to the fact that the states of the computational basis ([4.24](#br196)) are

transformed in accordance with the rule:

⎧

⎪|00
` `→ |00

⎪

,

⎪

⎪

⎨

|01
` `→ |01
` `,

(4.44)

⎪|10
` `→ |11

⎪

,

⎪

⎪

⎩

|11
` `→ |10
` `.

Note that the next element CNOT takes the input states in the reverse order

relative to the ﬁrst element. In this case, the basis state transformation rule has the

form:

⎧

⎪|00
` `→ |00

⎪

,

⎪

⎪

⎨

|01
` `→ |11
` `,

(4.45)

⎪|10
` `→ |10

⎪

,

⎪

⎪

⎩

|11
` `→ |01
` `.





Review Questions

191

Therefore, the next step of the quantum system evolution is described by the matrix

⎡

⎤

1 0 0 0

0 0 0 1

0 0 1 0

0 1 0 0

⎢

⎥

⎢

⎥

⎢

⎥

(4.46)

⎢

⎥ .

⎢

⎥

⎣

⎦

We perform the matrix computations:

⎡

⎤

⎡

⎤ ⎡

⎤

⎡

⎤

u1

1 0 0 0

0 0 0 1

0 0 1 0

0 1 0 0

u1

u1

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎢v1⎥

⎢

⎥ ⎢ 1⎥ ⎢ 2⎥

v

u

→

\=

.

(4.47)

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

v2

u2

v2

u2

v2

v1

⎣

⎦

⎣

⎦ ⎣

⎦

⎣

⎦

As a result, the original state |ψ ψ 

\=

[u , v , u , v ]T passes to

1

2

1

1

2

2

[u , u , v , v ]T . The matrix representation of the circuit under analysis can be

1

2

2

1

written in the form:

⎡

⎤ ⎡

⎤

⎡

⎤

1 0 0 0

0 1 0 0

0 0 0 1

0 0 1 0

1 0 0 0

0 0 0 1

0 0 1 0

0 1 0 0

1 0 0 0

0 0 0 1

0 1 0 0

0 0 1 0

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

\=

.

(4.48)

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥ ⎢

⎥

⎢

⎥

⎣

⎦ ⎣

⎦

⎣

⎦

**Review Questions**

\1. What is a complex number?

\2. Enumerate arithmetic operations on complex numbers.

\3. How is the number conjugate of a given complex number found?

\4. How can a complex number be presented geometrically?

\5. Explain the differences between the following forms of complex numbers:

algebraic, trigonometric and exponential.

\6. Write Euler’s formula.

\7. How is the root of the n-th order of a complex number found? How many values

does it take?

\8. Formulate the fundamental theorem of algebra.





192

4 Complex Numbers and Matrices

\9. What is Cardano formula used for?

\10. What matrices are called Hermitian? unitary?

\11. Deﬁne the concepts of “bit” and “qubit”.

\12. What states are referred to as the computational basis states?

\13. What is gate?

\14. Explain how the quantum state is measured.

\15. Write Pauli and Dirac matrices.

\16. Enumerate the basic operations on one qubit.

\17. What quantum operations are applied to a system of two qubits?

**Problems**

**4.1**. Perform algebraic manipulations and represent the speciﬁed complex num-

ber z in the algebraic form z = Re z + i Im z:

(1) (3 + i)(2 + 5i);

(2) (3 − i)(3 + i);

(3) (1 − i)4 + (1 + i)4;

(4) 2 − i3.

**4.2**. Perform algebraic manipulations and represent the speciﬁed complex num-

ber z in the algebraic form z = Re z + i Im z:

(1) (2 − i)(−1 + i);

(2) (6 + 5i)(4 − i);

(3) (1 + 3i)2 + (2 − i)2;

(4) i5 − i3.

**4.3**. Given are the complex numbers z = 5 + i, z = 4 − i, z = −1 + 3i. Find

1

2

3

2

z1z3 − z .

2

**4.4**. Given are the complex numbers z = 1 − 2i, z = −1 + i, z = −i. Find

1

2

3

3

3

3

1

z1z2(z − z ).

**4.5**. Perform the actions:

3

3

(1) (1 + 4i) + (1 − 4i) ;

4

4

(2) (6 − i) + (6 + i) .

a + ib

c + id

**4.6**. Having performed the division, represent the complex number z =

,

where a, b, c, d ∈ R, c = 0, d = 0, in algebraic form.

**4.7**. Simplify the expressions:

3 + i

(1)

(2)

;

3 − i

1 + 3i

1 − 3i

;





Problems

193

2 + i2

(3)

;

3 + i3

i

i

(4)

\+

.

1 + i

1 − i

**4.8**. Given are the complex numbers z = 2 + i, z = z∗, z = z + z . Find

1

2

3

1

2

1

(z1 − z3)(z2 − z3)/z2.

**4.9**. Given are the complex numbers z = 7 + 2i, z = −z , z = 2 − z∗. Find

1

2

1

3

1

(z1z2 + z2z3 + z1z3)/z1.

**4.10**. Find the number conjugate with the number z, if:

1 − 3i

(1) z =

;

1 + 3i

1

(2) z = 2i +

.

2 + i

**4.11**. Find z, if z − 3z∗ = 18 + 4i.

**4.12**. Find z, if 3z∗ − 7z = 10 − 10i.

**4.13**. Prove that for arbitrary z , z ∈ C the equalities are valid:

1

2

(1) (z + z )∗ = z∗ + z∗;

1

2

1

2

(2) (z z )∗ = z∗z∗.

1 2

1

2

**4.14**. Prove that if |z| = 1, then z−1 = z∗.

∗**4.15.** Prove that for any z , z ∈ C **triangle inequalities** are valid:

1

2


abs |z | − |z |  |z + z |  |z | + |z |.

1

2

1

2

1

2

∗**4.16.** Calculate the sums:

10

(1)

ik;

k=1

49

(2)

ik.

k=−49

**4.17**. Simplify the expression im for arbitrary m ∈ Z.

**4.18**. Represent the complex number in a trigonometric form:

(1) 2;

(2) 3i;

(3) 4 + 3i;

(4) −i;

(5) −3 − 6i;

√

(6) 2(1 + i);

√

(7) 3(−1 + 3i);

9 + i

(8)

.

9 − i





194

4 Complex Numbers and Matrices

**4.19**. Represent the following complex numbers in algebraic form z = Re z +

i Im z:

π

π

(1) z = cos + i sin

;

3

3

$

%

π

π

(2) z = 4 cos(− ) + i sin(− ) ;

2

2

√

3

(3) z =

;

3π

3π

cos

\+ i sin

4

4

π

π

(4) z = cos(− ) + i sin(− ).

8

8

a + ib

a − ib

**4.20**. Prove that a complex number of the type u =

, where a, b ∈ R, can

be presented in the form of an exponent with purely imaginary index, i. e. in

the form

u = eiδ,

δ

∈ R

.

**4.21**. Calculate ii.

**4.22**. Calculate:

√

(1) 8i;

√

(2) 6 4096.

∗**4.23.** Prove [the](#br421)[ ](#br421)[v](#br421)alidity of the identities for the roots of unity ω , where 0  k 

k

n − 1 [[24](#br421)[\]:](#br421)

(1) ω

= −ωk for even n and 0  k  n/2 − 1;

k+n/2

n−1

(2)

(3)

ωk = 0 for n > 1;

k=0

n−1

k=0

ωk = (−1)n−1 for all natural values n.

∗**4.24.** Prove the validity of the identities for the roots of unity ω , where 0  k 

k

n − 1, for all natural values n:

n−1

(1)

(z − ω ) = zn − 1;

k

k=0

n−1

0,

1

` `d  n − 1;

(2)

(ωk)d =

n, d = n.

k=0

∗**4.25.** Prove the validity of the identities for the n-th roots of unity ω , where k =

k

0, 1, . . . , n − 1, for all values n > 2:

n−2

(1)

ωkωk+1 = −ωn−1

;

k=0





Problems

195

n−2 ω

k−1

ωk

ωk+1

(2)

(3)

= −(1 + ωn−1);

k=1

n−1

ωkωk = 0;

=0

k,k

k<k

n−1 ω ω

k

n

k

(4)

\=

.

ω 

1 − ω2

=0

−

k

k,k

k<k

k

∗**4.26.** Let ω , where 0  k  n − 1, are the n-th roots of unity, x is an arbitrary

k

n−1

k=0

ω

k

complex number, and x = ωk for any k. Calculate the sum

.

x − ωk

∗**4.27.** Prove that [for](#br421)[ ](#br421)[n](#br421)atural n ∈ N and α = 2πk, k ∈ Z, are valid the **Lagrange’[s**](#br207)[**11](#br207)**

**identities** [[38](#br421)[\]:](#br421)

sin(nα/2)

(a) cosα + cos 2α + · · · + cos nα =

(b) sin α + sin 2α + · · · + sin nα =

cos[(n + 1)α/2];

sin[(n + 1)α/2].

sin (α/2)

sin(nα/2)

sin (α/2)

**4.28**. Prove de Moivre’s formula for natural values of the exponent n, using the

mathematical induction method.

∗**4.29.** Using de Moivre’s formula, express cos 3ϕ and sin 3ϕ in terms of cos ϕ and

sin ϕ.

∗**4.30.** Express cos 4ϕ and sin 4ϕ in terms of cos ϕ and sin ϕ.

∗**4.31.** There [exi](#br207)st relations that express polynomial’s coefﬁcients by its roots

(**Viète[**12](#br207)[ ](#br207)formulae**). If α , α , ..., α are roots of the polynomial p(z) =

1

2

n

x

n +

a1x

n−1 + · · · +

a

, and each root is taken the number of times

n

corresponding to its multiplicity, then the following equalities are valid:

α1 + α2 + · · · + αn = −a1,

α1α2 + α2α3 + · · · + α1α + α2α3 + · · · + α −1α = a2,

n

n

n

α1α2α3 + α1α2α4 + · · · + α −2α −1α = −a3,

. . .

n

n

n

α1α2 . . . α −1 + α1α2α −2α + · · · + α2α3 . . . α = (−1)n−1an−1,

n

n

n

n

α1α2 . . . α = (−1) a .

n

n

n

Prove validity of Viète formulae.

11Joseph-Louis Lagrange (1736–1813), French mathematician, mechanic and astronomer.

12François Viète, seigneur de la Bigotière (1540–1603), French mathematician.





196

4 Complex Numbers and Matrices

**4.32**. Let z , z be the roots of the quadratic trinomial p(z) = z2 +uz+v. Express

1

2

the following values by the coefﬁcients u and v:

(1) z2 + z2;

1

2

(2) z1−2 + z2

−2

.

**4.33**. Let z , z be the roots of the quadratic trinomial p(z) = z2 +uz+v. Express

1

2

the following values by the coefﬁcients u and v:

(1) z4 + z4;

1

2

−4

−4

(2) z + z

.

1

2

**4.34**. Find the sum and the product of all roots for each equation:

(1) z3 + 3z2 + 3z + 1 = 0;

(2) z4 + 10z2 + 20 = 0.

**4.35**. Find the sum and the product of all roots for each equation:

(1) z100 − 100z99 + z98 = 0;

(2) z5 + z4 + 1 = 0.

∗**4.36.** Compute the determinant




z1 z2 z3


` `= z z z


,

` `3

1

2




z2 z3 z1

where z , z and z are the roots of the cubic equation z3 + αz + β = 0 with

1

2

3

complex coefﬁcients α, β ∈ C.

∗**4.37.** Solve the equation z3 − 3z + 2 = 0, using the Cardano formula.

∗**4.38.** Solve the equation 2z3 − 13z2 − 17z + 70 = 0, using Cardano formula.

**4.39**. Solve the systems of linear equations using Cramer’s rule:

⎧

⎪ 1 +

\+ −2 + 2

−x1 + 3 −

\+ 1 +

= 1 −

= −7 + 2

⎪(

i)x1

(

i)x2

i)x2

(

i)x3

i)x3

i,

⎨

(a)

\+ 2 +

(

(

i,

⎪

⎪

⎩

(−2 − i)x1 + (−1 − i)x3 = 3 − 5i;

⎧

⎪ −2 + 2

\+ 2 +

i)x1

\+ 2 + 2

= 7

⎪(

i)x1

(

i)x2

(

i)x3

i,

⎨

(b)

−1 + 2

\+ −2 −

\+ 2ix3 = −8 + 2

(

(

i)x2

i,

⎪

⎪

⎩

(2 + 2i)x1 + 2ix2 + (1 − i)x3 = 2 + 4i;





Problems

197

⎧

⎪

−1 +

= 1 − 3

= 3 − 2

⎪

(

i)x3

i)x3

i,

i,

⎨

(c)

−1 +

−

\+ −1 −

(

i)x1 x2

(

⎪

⎪

⎩

x1 + (4 + i)x2 + (3 − i)x3 = 4 + 8i;

⎧

⎪ 4 +

i)x1 ix2 + 3x3 = −i,

−

⎪ (

⎨

(d)

3

\+ 4 + 1 −

= −4 + 9

x1

x2

(

i)x3

i,

⎪

⎪

⎩

ix1 + 3x2 + x3 = −5 + 6i.

**4.40**. Solve the systems of linear equations using Gaussian elimination:

⎧

⎪ 2 +

\+ 1 −

\+ 1 −

= 8

⎪(

i)x1

1 −

(

i)x2

(

i)x3

i,

⎨

(a)

(b)

(c)

(d)

\+ −1 +

\+

= −2

(

i)x1

(

i)x2 ix3

,

⎪

⎪

⎩

−ix + (3 + i)x + (−1 − i)x = 8 + 4i;

1

2

3

⎧

⎪ 4 −

\+ 4 −

−

= 2 + 9

⎪ (

i)x1

(

i)x2 ix3

i,

⎨

5

x1

\+ 3x2 = 5 + 10

2x + (2 + i)x + (1 + i)x = 3 + 5i;

−

ix3

i,

⎪

⎪

⎩

1

2

3

⎧

⎪ 1 + 2

\+ 3 + 2

\+ −2 + 2

= 11 +

= 8 + 3

⎪(

i)x1

(

i)x2

(

i)x3

i,

i,

⎨

(

4 −

i)x1

\+ −1 + 2

(

i)x2 x3

−

⎪

⎪

⎩

(1 + i)x1 + 2ix2 = 4 + 8i;

⎧

⎪5 + −2 −

\+ −3 −

= −12 −

= −3 +

⎪ x1

(

i)x2

(

i)x3

i)x3

i,

⎨

ix1

(

\+ 1 + 2

i)x2

\+ 2 −

(

i,

⎪

⎪

⎩

2ix + x = −4 + i.

2

3

∗**4.41.** Solve the systems of linear equations relative to ﬁve variables using Gaussian

elimination:

⎧

⎪

⎪(4 − i)x + ix + (−1 + i)x + (4 + 2i)x + (−3 + i)x = −5 − 9i,

⎪

1

2

3

4

5

⎪

⎪

⎪

⎪

2

−

− 3 + 2 −

\+ −2 −

= 3 − 5

⎪

x1 x2

x3

(

i)x4

(

i)x5

i,

⎨

(a)

(1 − i)x1 + (1 − i)x2 + (2 − i)x3 + (−2 − i)x4 + 3x5 = 10 + 11i,

⎪

⎪

⎪

⎪

⎪

(1 + 2i)x − 2x + (2 + 2i)x − 3x + (−2 + i)x = −2,

⎪

1

2

3

4

5

⎪

⎪

⎩

(−3 + 2i)x1 + x2 + (−2 + i)x3 − ix4 + 2ix5 = −11 + 3i;





198

4 Complex Numbers and Matrices

⎧

⎪

⎪

−3x + (−3 − i)x + (2 − i)x + (−2 + i)x + ix = −2 − i,

⎪

1

2

3

4

5

⎪

⎪

⎪

⎪

−x1

\+

(

\+ −3 + 2

i)x3

(

\+ 1 +

\+ 4 + 2

= 9 + 12

i,

⎪

ix2

i)x4

(

i)x5

⎨

(b)

2ix + (2 − i)x + 3x + 2x + (−2 − i)x = −9 − 5i,

1

2

3

4

5

⎪

⎪

⎪

⎪

⎪(−3 − i)x + (−3 − i)x + ix + (1 + i)x + (−1 + i)x = 4,

⎪

1

2

3

4

5

⎪

⎪

⎩

(2 + i)x1 + 2x2 + (1 + i)x3+(3 + 2i)x5 = −3 + 10i.

**4.42**. Which of the following matrices are Hermitian?

⎡

⎤

1

2 + 10i

(1) ⎣

⎦;

2 − 10i

3

⎡

⎤

1

1 −1

(2) √ ⎣

⎦;

2

−2 −2

⎡

⎤

1

2 + 2

2

i

i

(3) √ ⎣

⎦;

6

−2 −2 + 2

i

i

⎡

⎤

3 −i

(4) ⎣

⎦;

−i 3

⎡

⎤

1 0 2

1

⎢

⎥

(5) √ ⎢0 3 0 ⎥;

⎣

⎦

10

2 0 −i

⎡

⎤

1 1

1

1

⎢

⎥

⎢

⎥

1 i −1 −i

1 −1 1 −1

1 −i −1 i

⎢

⎥

(6)

.

⎢

⎥

⎢

⎥

⎣

⎦

**4.43**. What condition is imposed on the diagonal elements of the Hermitian

matrix?

**4.44**. Show that if Z and Z are complex matrices of the same order, then the

1

2

1

matrix (Z Z + Z Z ) is Hermitian.

1

2

2 1

2

**4.45**. **Anti-Hermitian** or **skew-Hermitian** matrix is the matrix A, for which the

relation AH = −A is fulﬁlled. In other words, Hermitian conjugate of such a

matrix results in multiplying all its elements by (−1). Which of the following





Problems

199

matrices are anti-Hermitian?

⎡

⎤

1

0

2 +

i

i

(1) √ ⎣

⎦;

2

−2 +

i

⎡

⎤

i −2

3 −2i

2 + i 2i

−2i −2 + i

(2) ⎣

⎦;

⎡

⎣

⎤

1

(3)

⎦;

3

⎡

⎤

1 5 0

1 ⎢

⎥

(4) ⎢−5 2 −5⎥;

i

⎣

⎡

⎦

⎤

5

0 5 3i

−2i 1 0

1 ⎢

⎥

(5) ⎢ −1 0 −3⎥;

⎣

⎦

5

0 3 2i

⎡

⎤

i i

i

i

⎢

⎥

⎢

⎥

−i −i

i −i i −i

i −i −i i

⎢i i

⎥

(6)

.

⎢

⎥

⎢

⎥

⎣

⎦

**4.46**. What condition is imposed on the diagonal elements of an anti-Hermitian

matrix?

**4.47**. Which of the following matrices are unitary?

⎡

⎤

1 2 3

(1) ⎣

⎦;

3 2 1

⎡

⎤

1

1 −

i

(2) √ ⎣

⎦;

2

−

i

1

⎡

⎤

1

3

2 +

2

i

i

(3)

⎣

⎦;

−2i −2 + i

⎡

⎤

1

3 −

−

i

(4) √

⎣

⎦;

10

i

3





200

4 Complex Numbers and Matrices

⎡

⎤

1 0

0

1

⎢

⎥

(5) √ ⎢0 2i 0 ⎥;

e

⎣

⎦

10

0 0 e4i

⎡

⎤

1 1

1

1

⎢

⎥

⎢

⎥

1

1

−1 −

⎢

i

i⎥

(6)

.

⎢

⎥

2 ⎢

⎥

1 −1 1 −1

1 −i −1 i

⎣

⎦

**4.48**. What condition must satisfy the complex numbers u and u and the real

⎡

⎤

1

2

u1

u2

number ϕ, in order for the matrix ⎣

⎦ to be unitary?

∗

2

iϕ

∗

1

−eiϕu e u

**4.49**. At the examination in linear algebra the student says that for any square

matrix A the equality ln(expA) = A is valid. Is the student right?

∗**4.50.** Prove the identity det(eA) = etr A, valid for the arbitrary square matrix A

with complex coefﬁcients.

**4.51**. Prove the Theorem 4.4 (see page [182](#br194)): the determinant of a unitary matrix is

a complex number, whose modulus is equal to one.

**4.52**. Compute the commutators of the Pauli matrices [σ , σ ], [σ , σ ] and

1

2

2

3

[σ , σ ].

3

1

**4.53**. Compute the product of the Pauli matrices σ σ σ .

1

2 3

∗**4.54.** Prove the generalization of **Euler’s identity** for Pauli matrices σ , σ and σ :

1

2

3

exp(iσ ϕ) = I cos ϕ + iσ sin ϕ for k = 1, 2, 3,

(4.49)

k

k

⎡

⎤

1 0

where I = ⎣ ⎦ is the identity matrix of the second order.

0 1

**4.55**. What is the square of the Dirac matrices β?

**4.56**. Compute the product of the Dirac matrices α α α β.

1

2 3

**4.57**. Compute the result of the actions of the quantum circuit

X

H

S

H

on a qubit that is originally in the state |0
.

**4.58**. Compute the result of the actions of the quantum circuit

Y

H

Z

T

on a qubit that is originally in the state |1
.





Answers and Solutions

201

**4.59**. Compute the result of the actions of the quantum circuit

T

H

S

H

S

on a qubit that is originally in the state |ψ
` `= u |0
` `+ v |1
, where u, v ∈ C.

**4.60**. Show that the quantum circuit

transfers the state |ψ ψ 
` `to the state |ψ ψ 
.

1

2

2 1

**Answers and Solutions**

[**4.1**](#br204)[** ](#br204)Solution.

(1) Operations with complex numbers should be performed similarly to the respec-

tive operations with algebraic polynomials, using the property i2 = −1:

(3 + i)(2 + 5i) = 3 · 2 + 3 · (5i) + i · 2 + i · (5i)

= 6 + 15i + 2i + 5i2 = 6 + 17i + 5(−1) = 1 + 17i;

(2) (3 − i)(3 + i) = 32 − i2 = 10;

(3) (1 − i)4 + (1 + i)4 = (1 − 4i + 6i2 − 4i3 + i4) + (1 + 4i + 6i2 + 4i3 + i4)




= 2 1 + 6i2 + (i2)2 = 2 1 + 6(−1) + (−1)2 = −8;

(4) 2 − i3 = 2 − i · i2 = 2 + i.

[**4.2**](#br204)[** ](#br204)Answer:

(1) −1 + 3i;

(2) 29 + 14i;

(3) −5 + 2i;

(4) 2i.

[**4.3**](#br204)[** ](#br204)Solution.

We perform algebraic transformations, taking into account that i2 = −1:

z1z3 − z

2 = 5 + −1 + 3 − 4 − 2 = 5 · −1 + 5 · 3 + · −1 + ·

(

i)(

i)

(

i)

(

)

( i) i (

)

i

2

(3i) − (16 − 8i + i )

2 = −8 + 14 − 15 + 8 = −23 + 22 .

i

i

i





202

4 Complex Numbers and Matrices

[**4.4**](#br204)[** ](#br204)Solution.

3

3

3

1

We perform algebraic manipulations: z z = 1 + 3i, z = i, z = −11 + 2i,

1

2

3

3

3

3

3

1

z − z = 11 − i. As a result z1z2(z − z ) = 14 + 32i.

3

1

[**4.5**](#br204)[** ](#br204)Solution.

(1) We perform algebraic transformations:

(1 + 4i)3 + (1 − 4i)3

2

2

= (1 + 4i + 1 − 4i)((1 + 4i) − (1 − 4i)(1 + 4i) + (1 − 4i) )

= 2(1 + 8i − 16 − 17 + 1 − 8i − 16) = −47 · 2 = −94.

(2) Use the Newton[13](#br214)[ ](#br214)binomial formula:

n

k=0

(a + b)n =

C(n, k)an−kbk,

valid for all a, b ∈ C and natural n:

4

4

4

3

2

(6 − i) + (6 + i) = 6 − 4 · 6 · i + 6 · 6 · (−1) − 4 · 6i · (−1) + (−1) · (−1)

4

3

2

\+ 6 + 4 · 6 · i + 6 · 6 · (−1) + 4 · 6i · (−1) + (−1) · (−1) = 2162.

[**4.6**](#br204)[** ](#br204)Solution.

z1

Denote z = a + ib, z = c + id. The fraction of the form , where z , z ∈ C,

1

2

1

2

z2

∗

2

∗

2

z

can be conveniently transformed by multiplying it by 1 ≡

:

z

∗

2

∗

2

∗

2

∗

2

∗

z1

z2

z1

z2

z1

z2

z

z

z1z

z1z

2

\=

· 1 =

·

\=

\=

.

z2z

|z2|2

This is why the result of the division of two complex numbers z /z , where

1

2

z2 = 0, will be the number

z1

z2

ac + bd

bc − ad

\=

\+ i

.

2 +

d

2

c

2 +

d

2

c

13Isaac Newton (1643–1727), English mathematician, physicist, mechanic and astronomer.





Answers and Solutions

203

[**4.7**](#br204)[** ](#br204)Solution.

∗

2

∗

2

2

Using the hint offered in the previous problem (i. e. z /z = (z z )/(z z ) =

1

2

1

∗

|

|2), we obtain

(3 + i)(3 + i)

(z1z )/ z2

2

3 + i

3 − i

1

5

(1)

(2)

\=

\=

(4 + 3i);

9 − i2

1 + 3i

(1 + 3i)2

1

\=

\=

\=

(−4 + 3i);

1 − 3i

2 + i2

1 − 9i2

2 − 1

5

1

(3)

(4)

\=

(3 + i);

3 + i3

3 + i2 · i

10

i

i

i(1 − i) + i(1 + i)

(1 + i)(1 − i)

\+

\=

= i.

1 + i

1 − i

[**4.8**](#br205)[** ](#br205)Solution.

Find z and z : z = 2 − i, z = (2 + i) + (2 − i) = 4. After this, we obtain

2

3

2

3

(z1−z3)(z2−z3)/z2 = (2+i−4)(2−i−4)/(2−i) = −(2−i)(−2−i)/(2−i) = 2+i.

[**4.9**](#br205)[** ](#br205)Solution.

Find z and z : z = −7 − 2i, z = −5 + 2i.

1

2

2

3

Then, z z = −45−28i, z z = 39−4i, z z = −39+4i, z z +z z +z z =

1

2

2

3

1

3

1

2

2

3

1 3

−45 − 28i.

The ﬁnal answer is (z z + z z + z z )/z = −7 − 2i.

1 2

2

3

1

3

1

[**4.10**](#br205)[** ](#br205)Answer:

1

(1) z = (−4 + 3i);

5

1

(2) z = (2 − 9i).

5

[**4.11**](#br205)[** ](#br205)Solution.

Let z = a +ib, then z−3z∗ = (a +ib)−3(a −ib) = −2a +4ib. Since complex

numbers are equal if and only if their real and imaginary parts are equal, we obtain


−2a = 18,

4b = 4;

a = −9,

b = 1,

⇔

whence z = −9 + i.

5

[**4.12**](#br205)[** ](#br205)Answer: z = − + i.

2

[**4.13**](#br205)[** ](#br205)Proof.

Let z = x + iy , z = x + iy , where x , x , y , y ∈ R.

1

1

1

2

2

2

1

2

1

2

(1) Express the left side of the equality by x , x , y and y :

1

2

1

2

∗

∗

(z1 + z2) = [(x1 + x2) + i(y1 + y2)] = (x1 + x2) − i(y1 + y2).





204

4 Complex Numbers and Matrices

Now transform its right side

∗

∗

2

z + z = (x1 − iy1) + (x2 − iy2) = (x1 + x2) − i(y1 + y2).

1

Therefore ∀z , z ∈ C (z + z )∗ = z∗ + z∗.

1

2

1

2

1

2

(2) The left side of the equality

∗

∗

(z1z2) = [(x1 + iy1)(x2 + iy2)] = (x1x2 − y1y2) − i(x1y2 + x2y1).

The right side coincides with the left one:

∗

∗

2

∗

z z = (x1 − iy1)(x2 − iy2) = (x1x2 − y1y2) − i(x1y2 + x2y1) = (z1z2) .

1

[**4.14**](#br205)[** ](#br205)Proof.

Take the number with the modulus equal to one in exponential form: z = eiϕ.

After algebraic transformations

z−1 = (e ) = e−iϕ = (e ) = z∗

iϕ −1

iϕ ∗

we obtain the equality z−1 = z∗.

[**4.15**](#br205)[** ](#br205)Hint.

Use the geometric interpretation of the numbers z and z . The length of a side

1

2

of an arbitrary triangle is no greater than the sum of the lengths of the two other

sides, and is no less than the absolute value of their difference.

[**4.16**](#br205)[** ](#br205)Solution.

Use the formula for the geometric progression sum:

n

k=1

n+1 −

.

q

q

qk =

q

\+ · · · +

qn =

q − 1

10

11 −

− −

i( i

−2 − − 1

i

i

i

i

)

(1)

(2)

ik =

49

\=

99

\=

= −1 + i.

i − 1

i − 1

(i − 1)(−i − 1)

k=1

1

ik =

i(k+49).

i49

k=−49

k=−99

In the last sum, replace the summation index k = k + 49. Then the sought sum

takes the following form:

49

98


99 − 1

i − 1

99 − 1

i − 1

−48−1 i

i

i

ik = i−49

= −i ·

i

k =

= − ·

i

k=−49

=0

i96 ·

k

i

3 − 1

i

3 − 1

i

4 −

i

1 −

i

= −i ·

= −

\=

= 1.

i − 1

i − 1

i − 1

i − 1





Answers and Solutions

205

[**4.17**](#br205)[** ](#br205)Solution.

The imaginary unit has the property i4 = 1. Consider four cases depending on

the remainder of division m by 4:

(1) m = 4k, k ∈ Z,

im = i4k = (i4)k = 1k = 1;

(2) m = 4k + 1, k ∈ Z,

(3) m = 4k + 2, k ∈ Z,

(4) m = 4k + 3, k ∈ Z,

Thus, we ﬁnally obtain

im =

im = i4k+1 = i4k ·

i

= 1 · = ;

i

i

im = i4k+2 = i4k · i2 = i2 = −1;

im = i4k+3 = i4k · i3 = −i.

⎧

⎪ 1

if = 4

∈ Z;

⎪

,

,

m

k, k

if m = 4k + 1, k ∈ Z;

if = 4 + 2 ∈ Z;

⎪

⎪

⎨

i,

⎪−1

⎪

m

k

, k

⎪

⎪

⎩

−i,

if m = 4k + 3, k ∈ Z.

[**4.18**](#br205)[** ](#br205)Solution.

(1) For transition to a trigonometric form of the complex number, we must

determine the modulus ρ = |z| and the argument ϕ = argz. Using the formulae

for ρ and ϕ, we obtain

\+

\-

ρ = x2 + y2 = 22 + 02 = 2,

y

ϕ = arctan + 2πk = 0 + 2πk = 2πk, k ∈ Z,

x

this is why the trigonometric form of the number 2 has the form

2(cos(2πk) + i sin(2πk)), where k ∈ Z.





206

4

Complex Numbers and Matrices

√

π

π

(2) ρ = 0 + 32 = 3, ϕ =

sgn(3) + 2πk =

\+ 2πk, therefore 3i =

2

2

$

$

%

$

%%

π

π

3 cos

\+ 2πk + i sin

\+ 2πk , k ∈ Z.

2

2


√

3

4

(3) ρ = 16 + 9 = 5, ϕ = arctan

\+ 2πk ,



3


3

4 + 3i = 5 cos arctan + 2πk + i sin arctan + 2πk , k ∈ Z.

4

4

π

π

(4) ρ = 1, ϕ = sgn(−1) + 2πk = − + 2πk;

2

2

−i = cos(π(2k − 1/2)) + i sin(π(2k − 1/2)), k ∈ Z.

√

√

(5) ρ = 9 + 36 = 3 5, ϕ = arctan 2 − π + 2πk,

√

−3 − 6i = 3 5(cos(arctan 2 + π(2k − 1)) + i sin(arctan 2 + π(2k − 1))),

k ∈ Z.

(6) ρ = 2, ϕ = π/4 + 2πk,

√

√

2 + 2i = 2(cos(π/4 + 2πk) + i sin(π/4 + 2πk)), k ∈ Z.

√

(7) ρ = 30, ϕ = arctan(−3) + π + 2πk,

√

√

√

− 3+3 3i = 30(cos(π −arctan 3+2πk))+i sin(π −arctan 3+2πk)),

k ∈ Z.

(8) Multiply the numerator and the denominator of the fraction by the value (9 + i)

and transform the obtained expression:

9 + i

9 − i

(9 + i)(9 + i)

(9 − i)(9 − i)

80 + 18i

40

9

\=

\=

\=

−

41 41

i,

82

,

$

%

$

$

%

40

41

2

9

2

9

ρ =

\+

= 1, ϕ = − arctan

\+ 2πk. We ﬁnally obtain

41

41

%

$

%

9 + i

9

9

= cos 2πk − arctan

\+ i sin 2πk − arctan

,

k ∈ Z.

9 − i

40

40

[**4.19**](#br206)[** ](#br206)Solution.

√

3

π

π

1

2

(1) cos + i sin

\=

\+

i;

3

3

2

$

%




π

π

(2) 4 cos −

\+ i sin −

= −4i;

2

3

2

√

√

√

6

6

(3)

= −

i −

;

3π

3π

2

2

cos

\+ i sin

4

4

\-

√

\-

√

2




2 +

2

2 −

π

π

(4) cos −

\+ i sin −

\=

−

i.

8

8

2

2





Answers and Solutions

207

[**4.20**](#br206)[** ](#br206)Proof.

Turn to the exponential form of the number u. Let a + ib = ρeiϕ, then a − ib =

−iϕ and

ρe

a + ib

a − ib

eiϕ

e−iϕ

u =

\=

= eiϕ · eiϕ = e2iϕ

.

Therefore u = eiδ, where δ = 2ϕ.

[**4.21**](#br206)[** ](#br206)Solution.

The exponential notation of the imaginary unit has the form i = eiπ/2+2πik,

where k ∈ Z. Having written the imaginary unit in the base in exponential form and

using the identity (ea)b = eab, we obtain

iπ/2+2πik i = i2(π/2+2πk) =

e

e

−

π/

2+2

πk where

,

k, k

∈ Z

.

ii = (e

)

As is seen from the considered example, the exponential function is a multifunc-

tion on the set of complex numbers C.

[**4.22**](#br206)[** ](#br206)Answer:

√

(1) 8i = ± 2(1 + i);

√

√

√

(2) 6 4096 ∈ {± 4, ± 2(1 ± i 3), ± 2(1 ∓ i 3)}.

[**4.23**](#br206)[** ](#br206)Proof.

(1) Transform the exponential notation of the number ωk+n/2

:

2πi(k+n/2)

2

πik

ωk+n/2 = e

= e

n eπi =

ωkeπi.

n

Using the equality eπi = −1, we obtain ω

0, 1, . . . , n/2 − 1.

= −ωk for even n and k =

k+n/2

(2) The values ω form a geometric progression, whose denominator is ω

\=

k

1

e

2πi/n. Using the formula for the geometric progression sum 1 +

q

\+

q

2 +

1 − qn+1

· · · + qn =

for |q| < 1, we obtain

1 − q

n−1

n

k=0

−1

(e

)

2πi/n n − 1

ωk =

e2πik/n

\=

= 0.

e πi/n − 1

2

k=0

(3)

n−1

n−1

n"−1

k=0

n"−1

2πik/n

(2πi

k)/n

ωk =

e2πik/n = ek=0

= e

k=0

.

k=0





208

4 Complex Numbers and Matrices

n−1

k=0

n(n − 1)

The sum in the exponent is

k =

, and therefore,

2

n"−1

k=0

ωk = eπi(n−1) = cos π(n

− 1 + sin

)

i

π(n

− 1 = −1 n−1

)

(

)

.

n

[**4.26**](#br207)[** ](#br207)Answer: xn − 1.

[**4.27**](#br207)[** ](#br207)Proof.

n

Consider the sum Z =

valid:

eiαk. It is easy to see that the following relations are

k=1

cos α + cos 2α + · · · + cos nα = Re Z,

sin α + sin 2α + · · · + sin nα = Im Z.

Calculate Z, using the formula for the geometric progression sum:

n

k=1

iα(n+1) −

eiα

e

Z =

eiαk =

.

eiα − 1

e−iα/2

e−iα/2

Simplify the obtained expression, multiplying the fraction by 1 =

and

performing simple transformations:

iα(n+1) −

eiα e−iα/2

e

iα(n+1/2) −

eiα/2

e

Z =

·

\=

.

eiα − 1

e−iα/2

e

iα/2 − −iα/2

e

Denominator of the obtained fraction is eiα/2 − e−iα/2 = 2i sin α/2. Rewrite the

exponents in the numerator, using Euler’s formula:


1

Z =

cos[(n + 1/2)α] + i sin[(n + 1/2)α] − (cos α/2 + i sin α/2)

2i sin α/2

sin[(n + 1/2)α] − sin α/2 cos[(n + 1/2)α] − cos α/2

\=

\+

.

2 sin α/2

2i sin α/2

Further, use the known trigonometric formulae (see Appendix B “Trigonometric

Formulae”, formulae ([B.16](#br418)) and ([B.18](#br418)))

a − b

2

a + b

2

sin a − sin b = 2 sin

cos a − cos b = −2 sin

cos

sin

,

a − b

2

a + b

.

2





Answers and Solutions

209

We obtain

sin(nα/2)

sin(nα/2)

sin[(n + 1)α/2],

sin (α/2)

Z =

cos[(n + 1)α/2] + i

sin (α/2)

whence directly follow the Lagrange’s identities.

[**4.28**](#br207)[** ](#br207)Proof.

Denote the predicate “(cos ϕ + i sin ϕ)n = cos nϕ + i sin nϕ” by P (n) and prove

the statement ∀n P (n) by the mathematical induction method.

B a s i s s t e p

For n = 1 we obtain the valid identity (cos ϕ + i sin ϕ)1 = cos ϕ + i sin ϕ,

therefore P(1) is true.

I n d u c t i v e s t e p

Suppose that P (k), k ∈ N is true. Prove the truth of the proposition P (k + 1).

We need to prove that

(cos ϕ + i sin ϕ)k+1 = cos (k

)ϕ

\+ 1 + sin + 1

i

(k

)ϕ.

Consider the expression (cos ϕ + i sin ϕ)k+1 and represent it in the form

(cos ϕ + i sin ϕ)

k+1 = cos + sin k · cos + sin

(

ϕ

i

ϕ)

(

ϕ

i

ϕ).

According to the inductive supposition, the ﬁrst factor is

(cos ϕ + i sin ϕ)k = cos kϕ

\+ sin

i

kϕ.

Then

(cos ϕ + i sin ϕ)

k+1 = cos

(

kϕ

\+ sin

i

· cos + sin

kϕ) (

ϕ

i

ϕ).

Open the brackets in the obtained expression, using the known identities for

trigonometric functions, provided in Appendix B, formulae [(](#br418)[B.11](#br418)) and ([B.9](#br417)):

cos(a + b) = cos a cos b − sin a sin b,

sin(a + b) = sin a cos b + cos a sin b,

assuming a = kϕ, b = ϕ. We obtain

(cos ϕ + i sin ϕ)

k+1 = cos

(

kϕ

cos − sin sin

cos (k+1)ϕ

ϕ

kϕ

ϕ)



!

\+ i (sin kϕ cos ϕ + cos kϕ sin ϕ) .



!

sin (k+1)ϕ





210

4 Complex Numbers and Matrices

Hence, according to the mathematical induction principle, de Moivre’s formula

(cos ϕ + i sin ϕ)n = cos nϕ

is valid for all natural values n ∈ N.

[**4.29**](#br207)[** ](#br207)Solution.

i

\+ sin

nϕ

Consider a more general case of the problem statement and express cos nϕ and

sin nϕ in terms and cosine and sine of the angle ϕ.

For this, note that in the left side of de Moivre’s formula ([4.1](#br185)) stands an

expression that can be expanded by the Newton binomial formula (see page [192](#br204)).

Thus, represent the left side in the form:

n

(cos ϕ + i sin ϕ)n =

C(n, j )(cosn−j ϕ)(i

sin ϕ)j

j=0

n

\=

ij C(n, j) cosn−j ϕ sinj ϕ.

j=0

It is convenient to partition the sum into two sums—by even (j = 2k) and odd

(j = 2k + 1) values of j, and introduce a new summation variable k ∈ N:

(cos ϕ + i sin ϕ)n

n/2

\=

i2kC(n, 2k) cosn−2k ϕ sin2k

ϕ

k=0

(n−1)/2

\+

i2k+1C(n, 2k + 1) cosn−2k−1 ϕ sin2k+1

ϕ

k=0

n/2

\=

(−1)kC(n, 2k) cosn−2k ϕ sin2k

ϕ

k=0

(n−1)/2

\+ i

(−1)kC(n, 2k + 1) cosn−2k−1 ϕ sin2k+1 ϕ.

k=0

Nown,we only have to take advantage of the fact that cos nϕ = Re (cos ϕ +

i sin ϕ)

sin nϕ = Im (cos ϕ +i sin ϕ)n. We obtain formulae for cosine and sine of a multiple





Answers and Solutions

211

argument:

n/2

cos nϕ =

sin nϕ =

(−1)kC(n, 2k) cosn−2k ϕ sin2k ϕ,

k=0

(n−1)/2

(−1)kC(n, 2k + 1) cosn−2k−1 ϕ sin2k+1 ϕ.

k=0

For n = 3 the obtained formulae take the form

1

cos 3ϕ =

sin 3ϕ =

(−1)kC(3, 2k) cos3−2k ϕ sin2k ϕ = cos ϕ − 3 cosϕ sin ϕ,

3

2

k=0

1

(−1)kC(3, 2k + 1) cos3−2k−1 ϕ sin2k+1 ϕ = 3 cos ϕ sin ϕ − sin ϕ.

2

3

k=0

[**4.30**](#br207)[** ](#br207)Answer:

2

cos 4ϕ =

(−1)kC(4, 2k) cos4−2k ϕ sin2k

ϕ

k=0

4

2

2

4

= cos ϕ − 6 cos ϕ sin ϕ + sin ϕ,

1

sin 4ϕ =

(−1)kC(4, 2k + 1) cos4−2k−1 ϕ sin2k+1

ϕ

k=0

3

3

= 4 cos ϕ sin ϕ − 4 cosϕ sin ϕ.

[**4.31**](#br207)[** ](#br207)Hint.

Multiply the brackets in the right side of factorization of the polynomial p(z) and

compare the obtained coefﬁcients at the same powers with the coefﬁcients p(z).

[**4.32**](#br208)[** ](#br208)Solution.

(1) Represent z2 + z2 in the form

1

2

2

2

2

z + z = (z1 + z2) − 2z1z2

1

2

and express the sum and the product of the roots p(z) by Viète formulae, proved

in the previous problem:

2

2

2

2

z + z = (−u) − 2v = u − 2v.

1

2





212

4 Complex Numbers and Matrices

2

1

2

2

2

1

1

\+

u − 2v

z

z

(2)

\+

\=

\=

.

2

2

2

2

2

2

z

z

z z

v

1

2

1

[**4.33**](#br208)[** ](#br208)Answer:

4

4

2

2

2

(1) z + z = (u − 2v) − 2v ;

1

2

1

1

(u2 − 2v)2 − 2v2

(2)

\+

\=

.

4

1

4

2

4

z

z

v

[**4.34**](#br208)[** ](#br208)Answer:

3

3

(1)

zk = −3,

zk = −1;

k=1

4

k=1

4

(2)

zk = 0,

zk = 20.

k=1

[**4.35**](#br208)[** ](#br208)Answer:

k=1

4

4

(1)

(2)

zk = 100,

zk = −1,

zk = 0;

k=1

5

k=1

5

zk = −1.

k=1

k=1

[**4.36**](#br208)[** ](#br208)Solution.

In the determinant, add to the ﬁrst row the second and the third rows:




\+ z + z z + z + z z + z + z

z1

2

3

1

2

3

1

2

3


` `=


.

z3

z1

z2





z2

z3

z1

According to Viète formulae (see Problem [**4.31**](#br207)), the sum of all roots of z +z +z

1

2

3

is equal to the coefﬁcient of the quadratic term z2, taken with reversed sign. For

the equation z3 + αz + β = 0 we have z + z + z = 0, and, therefore, in the

1

2

3

determinant  the ﬁrst row entirely consists of zero elements. It is clear that such a

determinant is equal to zero.

[**4.37**](#br208)[** ](#br208)Answer: z = −2, z = z = 1.

1

2

3

5

[**4.38**](#br208)[** ](#br208)Answer: z = 7, z = − , z = 2.

1

2

3

2

[**4.39**](#br208)[** ](#br208)Answer:

(a) [x , x , x ]T = [2i, −2, i]T ;

1

2

3

(b) [x , x , x ]T = [i, 1, 2 + 2i]T ;

1

2

3

(c) [x , x , x ]T = [−3, 3, −2 + i]T ;

1

2

3

(d) [x , x , x ]T = [1, −1 + 2i, −2 − i]T .

1

2

3





Answers and Solutions

213

[**4.40**](#br209)[** ](#br209)Answer:

(a) [x , x , x ]T = [2i, 1 + i, −2 + 2i]T ;

1

2

3

(b) [x , x , x ]T = [3 + 2i, −3 + i, 3 − i]T ;

1

2

3

(c) [x , x , x ]T = [2, 3 − i, −1 + 2i]T ;

1

2

3

(d) [x , x , x ]T = [−2 + 2i, 3i, 2 + i]T .

1

2

3

[**4.41**](#br209)[** ](#br209)Answer:

(a) [x , x , x , x , x ]T = [2 + i, i, −1 + i, −2, 1 + 2i]T ;

1

2

3

4

5

(b) [x , x , x , x , x ]T = [i, −2, −1 − i, 1 + i, 2 + 2i]T .

1

2

3

4

5

[**4.42**](#br210)[** ](#br210)Answer: Hermitian are matrices 1) and 2).

[**4.43**](#br210)[** ](#br210)Answer: diagonal elements of Hermitian matrix are valid.

[**4.44**](#br210)[** ](#br210)Proof.

1

Introduce the notation W = (Z Z + Z Z ) and ﬁnd Hermitian conjugate

1

2

2 1

2

matrix relative to W:


1

2

H

1

2

1

2

W

H =

(Z1Z2 Z2Z1)

\+

\=

((Z1Z2)H + (Z2Z1) )

H =

(Z2Z1 Z1Z2) W.

\+

\=

It is proved that W is a Hermitian matrix.

[**4.45**](#br210)[** ](#br210)Answer: anti-Hermitian are matrices (1), (5), (6).

[**4.46**](#br211)[** ](#br211)Answer: diagonal elements of anti-Hermitian matrix are purely imaginary

values.

[**4.47**](#br211)[** ](#br211)Answer: unitary are matrices (2), (3), (4), (6).

[**4.48**](#br212)[** ](#br212)Answer: |u |2 + |u |2 = 1, ϕ ∈ R is any real number.

1

2

[**4.49**](#br212)[** ](#br212)Solution.

In this case, the student is wrong, since for A = 2πiI, where I is the identity

matrix, we have exp(A) = e2πiI = I, therefore, ln(exp(A)) = O = A.

[**4.50**](#br212)[** ](#br212)Hint.

For the diagonal matrix det(eA) = eλ1eλ2 . . . eλ = etr A. As for the non-diagonal

n

matrix, we either diagonalize it, if possible, or, with any predeﬁned accuracy,

approximate it by a sequence of matrices, each being diagonalizable

[**4.51**](#br212)[** ](#br212)Proof.

Let U be an arbitrary unitary matrix. Using property (6) of Hermitian conjugate

on page [181](#br193), represent the modulus of the determinant U in the following form:

-(det U )(det U)∗ =

\-

(det U )(det UH ).

| det U| =





214

4 Complex Numbers and Matrices

Since the product of the determinants of matrices is equal to the determinant of their

product, ∀A, B (det A · det B = det(AB)), then

\-

√

| det U| = det(UUH ) = det I = 1.

Thus, the modulus of the determinant of the unitary matrix is equal to one.

[**4.52**](#br212)[** ](#br212)Answer: [σ , σ ] = 2iσ , [σ , σ ] = 2iσ , [σ , σ ] = 2iσ .

1

2

3

2

3

1

3

1

2

[**4.53**](#br212)[** ](#br212)Answer: σ σ σ = iI, where I is the identity matrix of size 2 × 2.

1

2 3

[**4.55**](#br212)[** ](#br212)Answer: β2 = I, where I is an identity matrix of size 4 × 4.

[**4.56**](#br212)[** ](#br212)Answer:

⎡

⎤

0 0 −i 0

0 0 0 −i

⎢

⎥

⎢

⎥

⎢

⎥

α1α2α3β = ⎢

⎥ .

⎢

⎥

i 0 0

0

⎣

⎦

0 i 0

0

[**4.57**](#br212)[** ](#br212)Solution.

⎡ ⎤

1

The state of the qubit |0
` `is described by the matrix ⎣ ⎦. Taking into account

0

the matrix representation of the quantum elements H, S and X from Table [4.1](#br200), we

obtain

⎡

⎤

⎡

⎣

⎤ ⎡

⎦ ⎣

⎤

⎦

⎡

⎣

⎤ ⎡ ⎤ ⎡ ⎤

1 − i

2

1

1 1

1 0

0

1

1 1

0 1

1

⎢

⎥

|ψ
` `→ |ψ
` `= √

√

⎦ ⎣ ⎦ ⎣ ⎦

\=

⎢

⎥

.

⎣

⎦

2

1 −1

2

1 −1

1 0

0

1 + i

i

2

Thus, as a result of the quantum circuit’s action on a qubit in the state |ψ
` `= |0
,

it passes to the state

1 − i

1 + i

|ψ
` `=

|0
` `+

|1
.

2

2

[**4.58**](#br212)[** ](#br212)Answer: as a result of the quantum circuit’s action on a qubit in the state |ψ
` `=

|1
, it passes to the state

$

%

$

%

i

1 − i

|ψ
` `= − √ |0
` `−

|1
` `.

2

2





Answers and Solutions

215

[**4.59**](#br213)[** ](#br213)Answer: a qubit in the state |ψ
` `= u |0
` `+ v |1
, passes to the state |ψ
` `=

[$](#br213)

%

$

%

1

2

1

1

2

1

(1 + i)u + √ v |0
` `+

(1 + i)u − √ v |1
.

2

2





**Chapter 5**

**Vector Spaces**

By n-**dimensional arithmetic vector**, we will mean an ordered set of n real

numbers.

The numbers x (i = 1, 2, . . . , n) are called **coordinates** or **components** of the

i

vector **x**. They are written either in the row: **x** = (x , x , . . . , x ), or in the column:

1

2

n

⎡

⎤

x1

x2

⎢

⎥

⎢

⎥

⎢

⎥

**x** = ⎢ ⎥ .

(5.1)

.

⎢ . ⎥

⎣ . ⎦

x

n

For designation of vectors a[nd](#br228)[ ](#br228)distinguishing them from scalar values, bold font

is used, for example, **a**, **b**, **c**, etc.[1](#br228)

The vectors **x** = (x , x , . . . , x ) and **y** = (y , y , . . . , y ) are called **equal**

1

2

n

1

2

n

**vectors**, if the equalities x = y , x = y , ..., x = y are valid.

1

1

2

2

n

n

**Sum** of the vectors **x** and **y** is the vector

**x** + **y** = (x + y , x + y , . . . , x + y ).

(5.2)

(5.3)

1

1

2

2

n

n

**Product** of the number α and a vector **x** is the vector

α**x** = (αx1, αx2, . . . , αxn).

1Another designation of vector is also used, when an arrow is placed above its symbol. For

−→

example, using this method, the vectors **a** and **b** will be designated as a and b .

−→

© Springer Nature Switzerland AG 2021

217

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_5>





218

5

Vector Spaces

**Difference** of the vectors **x** and **y** is the vector

**x** − **y** = **x** + (−1)**y** = (x − y , x − y , . . . , x − y ).

(5.4)

1

1

2

2

n

n

**Zero vector**, or **null vector**, is the vector **0** = (0, 0, . . . , 0) that has zero

coordinates. It is obvious that **x** + **0** = **x** − **0** = **x**.

For the vector **x** ∈ R, by −**x** denote the vector with the coordinates

(−x1, −x2, . . . , −xn),

(5.5)

such a vector being referred to as **opposite** relative to **x**.

From the introduced deﬁnitions, it follows that −**x** = (−1)·**x** and **x**+(−**x**) = **0**.

A set of all arithmetic vectors with the operations of addition and multiplication

intro[duced](#br421)[ ](#br421)on them is called a n-**dimensional arithmetic space** and denoted by

Rn [[30](#br421)[\].](#br421)

Example 5.1 R

1 is a one-dimensional space (line), R2 is a two-dimensional space

(plane) and R3 is a three-dimensional space.

**5.1 Linear Dependence of Vectors in the Space** R**n**

Consider a set of vectors **x** , **x** , . . . , **x**

k

∈

Rn and the real numbers

1

2

α1, α2, . . . , α ∈ R.

k

The vector **x** = α · **x** + α · **x** + · · · + α · **x** is called a **linear combination**

1

1

2

2

k

k

**of vectors x** , **x** , . . . , **x** .

1

2

k

Example 5.2 Let there be given the vectors

⎡

⎤

⎡ ⎤

⎡ ⎤

3

4

5

⎢

⎥

⎢ ⎥

⎢ ⎥

**x**1 = −2 , **x**2

⎢

⎥

= ⎢ ⎥

3

, **x**3

= ⎢ ⎥

3

.

(5.6)

⎣

⎦

⎣ ⎦

⎣ ⎦

−1

0

7

⎡

⎤

−1

⎢

⎥

Then, the vector **x** = 2**x** −3**x** +**x** = ⎢−10⎥ is the linear combination of vectors

1

2

3

⎣

⎦

5

**x** , **x** , **x** .

1

2

3

A system of vectors **x** , **x** , . . . , **x** is referred to as **linearly independent** one,

1

2

k

if from the equality α · **x** + α · **x** + · · · + α · **x** = **0**, it follows that α = α =

1

1

2

2

k

k

1

2

· · · = α = 0.

k





5.2 Basis in the Space Rn

219

If there exists a set of real numbers α , α , . . . , α , among which at least one is

1

2

k

not equal to zero, then the system of vectors is referred to as **linearly dependent**

one.

Example 5.3 Given are the vectors **x** = (2, −3) and **x** = (4, 5). Show that they

1

2

are linearly independent.

Find the solution of the system of equations

⎡

⎤

⎡ ⎤ ⎡ ⎤

2

4

0

⎣

⎦ + ⎣ ⎦ = ⎣ ⎦

(5.7)

(5.8)

α1

α2

,

−3

5

0

⎧

⎨

α1 · 2 + α2 · 4 = 0,

α1 · (−3) + α2 · 5 = 0.

⎩

Since this system has the unique solution α = α = 0, the vectors **x** and **x** are

1

2

1

2

linearly independent.

Note Assume that the vectors **x** , **x** , . . . , **x** are linearly dependent. Then, at least

1

2

k

one of the coefﬁcients α is other than zero (for example, α = 0). In this case, we

i

1

can write

α2

α3

αk

**x**1 = − **x**2 − **x**3 − · · · − **x** .

(5.9)

k

α1

α1

α1

Thus, if the vectors [are](#br421)[ ](#br421)linearly dependent, then one of them is linearly expressed

in terms of all others [[30](#br421)[\].](#br421)[ ](#br421)The converse is also true: if one of the vectors of the set is

linearly expressed in terms of the others, then these vectors are linearly dependent.

The last property can be considered as a deﬁnition of linear dependence of vectors.

**5.2 Basis in the Space** R**n**

Prior to introducing the concept of basis in the vector space Rn, let us prove the

following theorem.

**Theorem 5.1** Any system of n + 1 vectors in the space Rn is linearly dependent.

**Proof** Take arbitrary n + 1 vectors

**x** = (x , x , . . . , x ),

(5.10)

i

1i 2i

ni

where i = 1, 2, . . ., n + 1.





220

5

Vector Spaces

Construct their linear combination and equate it to zero vector:

α1 · **x**1 + α2 · **x**2 + · · · + α +1 · **x** +1 = **0**.

(5.11)

n

n

Writing this equality in a coordinate-wise manner, we arrive at a system of n

equations with n + 1 unknowns α , α , . . . , αn+1:

1

2

⎧

⎪

·

\+

·

\+ · · · +

αn+1 x1 +1

= 0

·

⎪ α1 x11 α2 x12

,

⎨

n

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

(5.12)

⎪

⎪

⎩

α1 · x 1 + α2 · x 2 + · · · + α +1 · xn n+1 = 0.

n

n

n

The matrix of the system ([5.12](#br231)) differs from the respective augmented matrix

only in the zero column, this is why their ranks coincide. Therefore, according to

the Kronecker–Capelli theorem, the system has inﬁnitely many solutions. They nec-

essarily include a non-zero solution. Thus, there exists a non-zero set of coefﬁcients

α1, α2, . . . , α +1, for which the linear combination of vectors **x**1, **x**2, . . . , **x** +1 is

n

n

equal to a non-zero vector. Therefore, the vectors **x** , where 1  i  n + 1, are

i

linearly dependent.

Any system of n linearly independent vectors **b** , **b** , . . . , **b** is called a **basis** of

1

2

n

a vector space.

Consider in the space Rn the system of vectors:

**e**1 = (1, 0, . . . , 0),

**e**2 = (0, 1, . . . , 0),

. . . . . . . . . . . . . . . . . .

**e**n = (0, 0, . . . , 1).

(5.13)

(5.14)

These vectors are linearly independent, since from the condition

α1 · **e**1 + · · · + α · **e** = **0**

n

n

directly follows the system of equalities α = α = · · · = α = 0.

1

2

n

The vectors **e** , **e** , ..., **e** are called **normalized vectors** of the space Rn; they

1

2

n

form the basis in this space.

**Conclusion**: a linearly independent system of vectors in Rn can have a maximum

of n vectors.

Consider a system of n vectors

**x** = (x , x , . . . , x ), where i = 1, 2, . . . , n.

(5.15)

i

1i 2i

ni





5.2 Basis in the Space Rn

221

Construct a matrix of coordinates of the vectors:

⎡

⎤

x11 x12 . . . x1n

x21 x22 . . . x2

⎢

⎥

⎢

⎥

⎢

n⎥

(5.16)

⎢

⎥ .

.

.

.

.

⎢

⎥

.

.

.

.

⎣ .

.

.

.

⎦

x 1 x 2 . . . x

n

n

nn

Such a matrix is called a **matrix of a system of vectors**, and its determinant is

called a **determinant of a system of vectors**.

**Theorem 5.2** In order for a system of n vectors to be the basis, it is necessary and

sufﬁcient that the determinant of the system is other than zero.

**Proof** Consider an arbitrary system of n vectors

**x** = (x , x , . . . , x ), i = 1, 2, . . ., n.

(5.17)

(5.18)

i

1i 2i

ni

Construct their linear combination and equate it to zero vector:

⎡

⎤

⎡ ⎤

α1 · x11 + α2 · x12 + · · · + α · x1

0

n

n

⎢

⎥

⎢ ⎥

⎢

⎥

⎢ ⎥

· x21 + α2 · x22 + · · · + αn · x

n

0

⎢ α1

2 ⎥ ⎢ ⎥

\=

.

⎢

⎥

⎢ ⎥

.

⎢

⎥

⎢.⎥

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎣

⎦

⎣.⎦

α1 · x 1 + α2 · x 2 + · · · + α · x

0

n

n

n

nn

We will obtain a homogeneous system of n equations with n unknowns and a

determinant other than zero. In this case, such a system has only a zero solution, i.e.

αi = 0, where i = 1, 2, . . ., n, and the system of vectors is a basis.

**Theorem 5.3** Assume that the vectors **x** , **x** , . . . , **x** form a basis. Then, any

1

2

n

vector **y** of Rn can be represented, uniquely, in the form of a linear combination

of the vectors **x**i (i = 1, 2, . . . , n):

**y** = α · **x** + α · **x** + · · · + α · **x** .

(5.19)

1

1

2

2

n

n

**Proof** Write the expansion ([5.19](#br232)) in projections:

⎡

⎤

⎡

⎤

α1 · x11 + α2 · x12 + · · · + αn · x1n

y1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

· x21 + α2 · x22 + · · · + αn · x

n

y2

⎢ α1

2 ⎥

⎢

⎥

α1**x**1 + α2**x**2 + · · · + α **x** = ⎢

⎥ = ⎢ ⎥ .

n

n

.

⎢

⎥

⎢ . ⎥

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

⎣

⎦

⎣ . ⎦

α1 · x 1 + α2 · x 2 + · · · + α · x

n

n

n

nn

y

n

(5.20)





222

5 Vector Spaces

We have obtained a non-homogeneous system of n equations with n unknowns.

Since the determinant of this system is other than zero, by virtue of Cramer’s rule,

this system has the unique solution.

Note The formula ([5.19](#br232)) is called an **expansion of the vector y in the basis x** (i =

i

1, 2, . . ., n).

Example 5.4 Show that the vectors **a** = (1, 1, 4), **b** = (0, −3, 2) and **c** =

(2, 1, −1) form a basis.

Construct the determinant of the system of vectors and compute it:





1 0

2





` `= 1 · 3 − 2 + 2 · 2 + 12 = 29

(5.21)

1 −3 1

(

)

(

)

.



4 2 −1

Since the determinant of the system is other than zero, the vectors **a**, **b** and **c**

form a basis.

Example 5.5 Expand the vector **d** = (6, 5, −14) in the basis (**a**, **b**, **c**) (see previous

example).

Represent the vector **d** in the form of the expansion:

**d** = α · **a** + α · **b** + α · **c**.

(5.22)

1

2

3

We have

⎡

⎤

⎡ ⎤

⎡

⎤

⎡

⎤

6

5

1

0

2

1

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

⎢

⎥ = ⎢ ⎥ +

⎢

⎥ +

⎢

⎥

(5.23)

α1

1

α2 −3

α3

.

⎣

⎦

⎣ ⎦

⎣

⎦

⎣

⎦

−14

4

2

−1

Write this equality in the form of the system of linear equations:

⎧

⎪

+2α3

\=

6

,

⎪ α1

⎨

α1 −3α2 +α3 =

4α1 +2α2 −α3 = −14.

5,

(5.24)

⎪

⎪

⎩

The obtained system has the unique solution α = −2, α = −1, α = 4. Thus,

1

2

3

**d** = −2**a** − **b** + 4**c**.






5.3 Euclidean Vector Space

223

**5.3 Euclidean Vector Space**

In an arbitrary n-dimensional vector space, it is possible to introduce a **scalar**

**product** (known also as **inner product**, or **dot product**)—the rule according to

which the two vectors **a**, **b** ∈ Rn are associated with the number (**a** · **b**). The scalar

product suggests such analogues of a spatial arrangement of the multidimensional

vectors Rn as orthogonality and collinearity.

By deﬁnition, the scalar product of the vectors **a** = (a , a , . . . , a ) and **b** =

1

2

n

(b1, b2, . . . , b ) is computed by the formula:

n

(**a** · **b**) = a1b1 + a2b2 + · · · + a b .

(5.25)

n

n

Note that with the help of the summation sign, the variable (**a** · **b**) is compactly

n

written as (**a** · **b**) =

a b .

i i

i=1

Let us enumerate the properties of a scalar product.

For arbitrary **a**, **a** , **a** , **b** ∈ Rn and α ∈ R, the following equalities are valid:

1

2

(1) (**a** · **b**) = (**b** · **a**) (symmetry);

(2) ((**a** + **a** ) · **b**) = (**a** · **b**) + (**a** · **b**) (linearity);

1

2

1

2

(3) (α**a** · **b**) = α(**a** · **b**) (linearity);

(4) (**a** · **a**)  0, and (**a** · **a**) = 0 ⇔ **a** = **0** (non-negativity).

Note For the scalar product of the vectors **a** and **b**, the designations (**a**, **b**), **a** · **b** or

**ab** are also used.

Example 5.6 Let n = 4, and in the coordinate notation, the vectors have the form,

**a** = (10, −2, 1, 9), **b** = (0, 3, 4, −2) and **c** = (−12, 2, −4, −5). Then,

**a** · **b** = 10 · 0 + (−2) · 3 + 1 · 4 + 9 · (−2) = −20,

**a** · **c** = 10 · (−12) + (−2) · 2 + 1 · (−4) + 9 · (−5) = −173,

**b** · **c** = 0 · (−12) + 3 · 2 + 4 · (−4) + (−2) · (−5) = 0.

Example 5.7 Show that if the condition (**a** · **t**) = (**b** · **t**) is valid for all **t** ∈ Rn, then

the vectors **a** and **b** are equal to each other.

**Proof** Based on the property of linearity, represent the equality (**a** · **t**) = (**b** · **t**) in

the equivalent form

(**a** · **t**) = (**b** · **t**) ⇔ ((**a** − **b**) · **t**) = 0.

(5.26)

Into the obtained equality, substitute **t** = **a** − **b**. Then, according to the property

of non-negativity, we have (**a** − **b**) = **0** or **a** = **b**, which is what we set out to

prove.






224

5 Vector Spaces

√

**Length**, or **norm**, of a vector is the value **a** = (**a** · **a**).

Note the following easily provable properties of the norm, which are valid for

arbitrary vectors **a** and **b** of Euclidean space:

(1) **a**  0, and **a** = 0 ⇔ **a** = 0;

(2) α**a** = abs(α)**a** for all α ∈ R;

(3) **a** + **b**  **a** + **b**.

The last inequality is referred to as a **triangle inequality** or **Minkow[ski**](#br235)[**2](#br235)**

**inequality**.

Example 5.8 For the vectors **a** = (0, −1, −1, 3, 1) and **b** = (5, −3, 0, −2, −1) in

the space R5, we have

\-

\-

√

**a** = (**a** · **a**) = 0 + (−1)2 + (−1)2 + 32 + 12 = 12;

\-

\-

√

**b** = (**b** · **b**) = (−5)2 + (−3)2 + 02 + (−2)2 + (−1)2 = 39.

**Orthogonal** are the vectors whose scalar product is equal to zero. Usually, the

orthogonal vectors are designated as **a** ⊥ **b**.

A set of vectors, where all vectors are pairwise orthogonal, is naturally called

**orthogonal**. If in such a set all vectors have a unit norm, then such a set is

**orthonormal**.

Of course, in an arbitrary basis, the vectors might not possess the property of

pairwise orthogonality, a fortiori orthonormality. Show that there exists a possibility

to construct a new basis from the original one, and in the new basis, al[l](#br235)[ ](#br235)the vect[ors](#br235)

will be pairwise orthogonal. Such a procedure is called the **Gram[**3](#br235)–S[chmidt**](#br235)[**4](#br235)**

**process** (orthogonalization).

Assume that in a vector Euclidean space with a norm, a basis (**p** , **p** , . . . , **p** ) is

1

2

n

set. The procedure of constructing a new orthonormal basis consists in performing

the following steps.

Successively compute the vectors **q** , **q** , . . . , **q** by the formulae:

1

2

n

**t**1

**t**1

**t** = **p** , **q**1 =

,

1

1

**t**2

**t**2

**t** = **p** − (**p** , **q** )**q** , **q**2 =

,

2

2

2

1

1

2Hermann Minkowski (1864–1909), German mathematician.

3Jørgen Pedersen Gram (1850–1916), Danish mathematician.

4Erhardt Schmidt (1876–1959), German mathematician.





5.4 Eigenvalues and Eigenvectors of a Matrix

225

**t**3

**t**3

**t** = **p** − (**p** , **q** )**q** − (**p** , **q** )**q** , **q**3 =

,

3

3

3

1

1

3

2

2

. . .

**t**n

**t**n

**t** = **p** − (**p** , **q** )**q** − · · · − (**p** , **q**n−1)**q**n−1

,

**q**n =

.

n

n

n

1

1

n

The obtained basis (**q** , **q** , . . . , **q** ) is orthonormal.

1

2

n

**5.4 Eigenvalues and Eigenvectors of a Matrix**

Two matrices A and A, bound by the relation

A = P−1AP,

(5.27)

where P is some invertible matrix, are referred to as **similar**. In this case, the

designation A ∼ A is used.

Note Transition from the matrix A to A is called **similarity transformation**.

⎡

⎤

⎡

⎤

1 −3

−1 2

−2 1

−9 5

Example 5.9 Matrices ⎣

⎦ and ⎣

⎦ are similar, since the following

equality is valid:

⎡

⎤

⎡

⎤

⎡

⎤ ⎡

⎤

−1

−2 1

−9 5

1 −1

−2 1

1 −3

−1 2

1 −1

−2 1

⎣

⎦ = ⎣

⎦

⎣

⎦ ⎣

⎦

(5.28)

.

⎡

⎤

⎡

⎤

−1

1 −1

−2 1

−1 −1

−2 −1

Indeed, ⎣

⎦

= ⎣

⎦, and the equality ([5.28](#br236)) is easily veriﬁed by

a direct multiplication of the matrices.

**Theorem 5.4 (On the Matrix Similarity Properties)** The following properties of

similarity are valid:

(1) A ∼ A—reﬂexivity;

(2) A ∼ B ⇒ B ∼ A—symmetry;

(3) ((A ∼ B) **and** (B ∼ C)) ⇒ (A ∼ C)—transitivity.

It follows from the theorem on the [ma](#br420)[trix](#br421)[ ](#br421)[sim](#br422)ilarity properties that the similarity

of matrices is an equivalence relation [[1](#br420)[,](#br420)[ ](#br420)[41](#br421)[,](#br421)[ ](#br421)[53](#br422)].





226

5 Vector Spaces

Two similar matrices have equal determinants. Indeed, from the deﬁnition

of ([5.27](#br236)), it follows that

|A| = |P−1AP| = |P−1| |A| |P| = |A|.

(5.29)

Note that the equality of the determinants does not at all imply the similarity of

the matrices.

⎡

⎤

0 1

Example 5.10 Find out whether the following matrices are similar: ⎣ ⎦ and

1 0

⎡

⎣

⎤

1 0

⎦.

1 1

The determinants of these matrices are equal to −1 and 1, respectively. Therefore,

these matrices do not possess the property of similarity.

The number λ and the non-zero vector **b** are referred to as **eigenvalue** and

**eigenvector** of the matrix A, respectively, if the following equality is valid:

A**b** = λ**b**.

(5.30)

The vector **b** is considered as a column vector. In order to ﬁnd **b** and λ, represent

Eq. ([5.30](#br237)) in the following form:

(A − λI )**b** = 0,

(5.31)

where I is an identity matrix.

We have obtained a homogeneous system of linear equations. In order for it to

have a non-zero solution, it is necessary and sufﬁcient that the determinant of the

matrix A−λI is equal to zero. Thus, in order to ﬁnd λ, we should solve the equation

|A − λI| = 0

(5.32)

or, in an expanded notation




− λ a12 . . .

a21 a22

a

a1n

a2

11




− λ . . .


n

= 0.

(5.33)




. . . . . . . . . . . . . . . . . . . . . . . . . . .





−

a 1

n

an2 . . . ann

λ

This equation is referred to as **characteristic equation**.





5.4 Eigenvalues and Eigenvectors of a Matrix

227

If we expand the determinant, we obtain a polynomial of power n relative to the

variable λ:

p(λ) = (−λ)n + h1( λ)

−

n−1 + · · · +

h −1( λ) h ,

−

\+

(5.34)

n

n

and the following properties are valid:

• the coefﬁcient h is equal to the trace of the matrix A: h = tr A = a + a22

nn

\+

1

1

11

· · · + a ;

• the constant term h coincides with the determinant: h = det A.

n

n

The polynomial ([5.34](#br238)) is also referred to as **characteristic**.

It is known that characteristic polynomials of similar matrices coincide.

According to the fundamental theorem of algebra, the characteristic equa-

tion ([5.30](#br237)) has no more than n solutions. For each solution λ, it is associated with

the eigenvector **b**.

Note Although the eigenvalue can be equal to zero, the eigenvector, by deﬁnition,

is always different from the zero vector.

Example 5.11 Find the eigenvalues and eigenvectors of the matrix

⎡

⎤

1 1 3

⎢

⎥

A = 1 5 1

⎢

⎥

.

(5.35)

⎣

⎦

3 1 1

Compute the determinant of the matrix A − λI and equate it to zero:




1 − λ

1

5 −

1

3

1




|A − λI| = 

1

λ





3

1 −

λ

= (1 − λ) · [(5 − λ) · (1 − λ) − 1] − (1 − λ) + 3 + 3 · [1 − 3 · (5 − λ)]

2

3

2

= (1 − λ) · (λ − 6 · λ + 3) + 9 · λ − 39 = −λ + 7 · λ − 36

= −(λ + 2) · (λ2 − 9 · λ + 18) = 0.

Solving this equation, we will obtain three roots, λ = −2, λ = 6 and λ = 3.

1

2

3

For each λ, ﬁnd the eigenvector associated with it.

\1. Let λ = −2. Then,

⎡

⎤

3 1 3

⎢

⎥

A − λ1I = 1 7 1

⎢

⎥

.

(5.36)

⎣

⎦

3 1 3





228

5 Vector Spaces

Assuming that **b** = (x, y, z), we will obtain the system of equations

⎧

⎪3 + + 3 = 0

⎪ x

y

z

,

⎨

x + 7y + z = 0,

3x + y + 3z = 0.

(5.37)

(5.38)

(5.39)

⎪

⎪

⎩

Write the matrix that corresponds to this system:

⎡

⎤

3 1 3

1 7 1

3 1 3

⎢

⎥

⎢

⎥

.

⎣

⎦

Add to the third row of this matrix the second one, multiplied by (−1):

⎡

⎤

3 1 3

1 7 1

0 0 0

⎢

⎥

⎢

⎥

.

⎣

⎦

Drop the zero row and exchange places of the second and the ﬁrst rows. Then,

we have

⎡

⎣

⎤

⎦

1 7 1

3 1 3

.

(5.40)

Bring the matrix to echelon form; add to the second row the ﬁrst one,

multiplied by −3. We obtain

⎡

⎤

1

7 1

⎣

⎦

(5.41)

.

0 −20 0

Proceed to the equations and write

⎧

⎨

x +7y +z = 0,

(5.42)

⎩

y

= 0,

or x + z = 0.

As a free variable, select z. Then, assume that z = 1, and then x = −1.

Thus, **b** = (−1, 0, 1).

1





5.4 Eigenvalues and Eigenvectors of a Matrix

229

\2. For λ = 6, we obtain the system:

⎧

⎪ −5 + + 3 = 0

⎪

x

y

z

,

⎨

x − y + z = 0,

3x + y − 5z = 0.

(5.43)

⎪

⎪

⎩

In order to ﬁnd the vector **b** , write the matrix of this system and its

2

transformations:

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

⎦

−5 1

3

1 −1 1

1 −1 1

0 −4 8

0 4 −8

⎢

⎥

⎢

⎥

⎢

⎥

1 −1 1

0 1 −2

⎢

⎥ → ⎢

⎥ → ⎢

⎥ → ⎣

1 −1 1

−5 1

3

.

⎣

⎦

⎣

⎦

⎣

⎦

3

1 −5

3

1 −5

Proceed to the system of equations:

⎧

⎨

x − y = −z,

y = 2z.

(5.44)

⎩

Assuming that z = 1, we ﬁnd y = 2 and x = 1.

Thus, **b** = (1, 2, 1).

2

\3. For λ = 3, we have the system:

⎧

⎪ −2 + + 3 = 0

⎪

x

y

z

,

⎨

x + 2y + z = 0,

3x + y − 2z = 0.

(5.45)

⎪

⎪

⎩

In order to ﬁnd the vector **b** , we perform similar equivalent transformations:

3

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

⎦

−2 1 3

1 2 1

3 1 −2

1 2 1

−2 1 3

3 1 −2

1 2

1

5

⎢

⎥

⎢

⎥

⎢

⎥

1 2 1

⎢

⎥ → ⎢

⎥ → ⎢

⎥ → ⎣

0 5

.

⎣

⎦

⎣

⎦

⎣

⎦

0 1 1

0 −5 −5

Proceed to the system of equations:

⎧

⎨

x + 2y = −z,

y = −z.

(5.46)

⎩

Assuming that z = 1, we ﬁnd y = −1 and x = 1.





230

5 Vector Spaces

Thus, the matrix A has the following eigenvalues and eigenvectors corre-

sponding to them:

λ1 = −2, **b**1 = (−1, 0, 1),

λ2 = 6, **b**2 = (1, 2, 1),

λ3 = 3, **b**3 = (1, −1, 1).

(5.47)

(5.48)

(5.49)

Note In physics, the characteristic equation is sometimes referred to as the **secular**

**equation** since such equations appeared during the analysis of the motion of the

Solar system’s planets and [th](#br420)eir satellites over considerable periods of time (referred

to as “secular” motions) [[2](#br420)].

**Annihilating polynomial** for the matrix A is such polynomial p(x) whose value

of this matrix is equal to the zero matrix: p(A) = O.

**Theorem 5.5 (Cayley[**5](#br241)–Hamilton[**6](#br241)[ ](#br241)Theorem)** Fo r any square matrix A, the char-

acteristic polynomial is its annihilating polynomial.

Example 5.12 Let us illustrate the Cayley–Hamilton theorem with the help of the

⎡

⎤

1 −10

characteristic polynomial of the matrix A = ⎣

⎦.

−6

5




1 − −10 

λ

Indeed, p(λ) = det |A − λI| = 

` `= λ2 − 6λ − 55.


` `−6 5 − λ

Check whether the equality p(A) = O is valid:

⎡

⎤

⎡

⎤

⎡

⎤

2

1 −10

1 −10

1 0

p(A) =

⎣

⎦ − 6 ⎣

⎦ − 55 ⎣

⎦

−6

5

−6

5

0 1

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

61 −60

−36 85

−6 60

36 −30

−55

0

0 0

= ⎣

⎦ + ⎣

⎦ + ⎣

⎦ = ⎣ ⎦ .

0

−55

0 0

Then, p(λ) is the annihilating polynomial for the matrix A.

Recall that the similar matrices A and B are bound by the relation B = P−1AP

for some nonsingular matrix P. Selecting P composed of the columns equal to the

eigenvectors A (written in random order), we obtain the diagonal matrix B. This is

the point of the procedure of **diagonalization** of the initial matrix.

5Arthur Cayley (1821–1895), English mathematician.

6William Rowan Hamilton (1805–1865), Irish mathematician and physicist.





Problems

231

Note that the sufﬁcient condition for the possibility of diagonalization is the

presence of different eigenvalues of the initial matrix, and their number should

coincide with its order.

**Review Questions**

\1. Deﬁne n-dimensional arithmetic vector.

\2. Enumerate the basic operations of vectors.

\3. What is n-dimensional arithmetic space?

\4. How is a linear combination of a system of vectors constructed?

\5. What system of vectors is referred to as linearly dependent?

\6. Deﬁne basis of a vector space.

\7. Formulate the criterion that an arbitrary system of vectors is the basis.

\8. Explain how a scalar product of vectors can be introduced into a vector space.

\9. Enumerate the basic properties of a scalar product.

\10. How is the norm of a vector found?

\11. What is the Gram–Schmidt orthogonalization procedure used for?

\12. What two matrices are called similar?

\13. Enumerate the properties of similarity of matrices.

\14. Deﬁne the concepts of “eigenvector” and “eigenvalue” of a matrix.

\15. How can one, knowing the elements of the matrix, set up its characteristic

equation?

\16. Formulate the Cayley–Hamilton theorem.

\17. What is the sufﬁcient condition of diagonalization of a matrix?

**Problems**

**5.1.** Find out whether the vectors **p**, **q** and **r** form a basis in a three-dimensional

vector space. If they do, expand the vector **x** in this basis.

⎡ ⎤

⎡ ⎤

⎡ ⎤

⎡ ⎤

2

1

4

3

⎢ ⎥

⎢ ⎥

⎢ ⎥

⎢ ⎥

(1) **p** = ⎢1⎥ , **q** = ⎢0⎥ , **r** = ⎢2⎥ , **x** = ⎢1⎥ .

(5.50)

(5.51)

⎣ ⎦

⎣ ⎦

⎣ ⎦

⎣ ⎦

0

1

1

3

⎡ ⎤

⎡

⎤

⎡

⎤

⎡

⎤

5

2

1

13

⎢ ⎥

⎢

⎥

⎢

⎥

⎢

⎥

(2) **p** = ⎢1⎥ , **q** = ⎢−1⎥ , **r** = ⎢ 0 ⎥ , **x** = ⎢ 2 ⎥ .

⎣ ⎦

⎣

⎦

⎣

⎦

⎣

⎦

0

3

−1

7





232

5

Vector Spaces

⎡ ⎤

⎡

⎤

⎡

⎤

⎡

⎤

4

2

−1

−9

⎢ ⎥

⎢

⎥

⎢

⎥

⎢

⎥

(3) **p** = ⎢1⎥ , **q** = ⎢ 0 ⎥ , **r** = ⎢ 2 ⎥ , **x** = ⎢ 5 ⎥ .

(5.52)

⎣ ⎦

⎣

⎦

⎣

⎦

⎣

⎦

1

−3

1

5

**5.2.** The vectors **e** , **e** , **e** and **e** are speciﬁed by their coordinates in some basis.

1

2

3

4

Show that the vectors **e** , **e** , **e** and **e** themselves form a basis, and ﬁnd the

1

2

3

4

coordinates of the vector **x** in this basis:

⎡

⎤

⎡

⎤

⎡ ⎤

⎡

⎤

⎡

⎤

1

2

2

3

1

1

3

7

14

−1

2

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

2

⎢

⎥

⎢

⎥

⎢ ⎥

⎢

⎥

⎢

⎥

**e** = ⎢ ⎥ , **e** = ⎢ ⎥ , **e** = ⎢ ⎥ , **e** = ⎢ ⎥ , **x** = ⎢ ⎥ .

1

2

3

4

⎢

⎥

−1

−2

⎢

−1

⎥

⎢ ⎥

⎢

⎥

−1

0

⎢

⎥

0

1

⎣

⎦

⎣

⎦

⎣ ⎦

⎣

⎦

⎣

⎦

4

(5.53)

**5.3.** Check that the vectors **a** = (1, 2, 3), **b** = (−3, −2, 3) and **c** = (0, −2, −2)

are linearly independent and thus form a basis. Is it orthogonal? Is it

orthonormal? If the answers are negative, then use the Gram–Schmidt

orthogonalization process to construct an orthonormal basis.

**5.4.** Check that the vectors **a** = (3, −1, 1, 2), **b** = (−3, 1, 0, −2), **c** =

\4. Is it orthogonal?

(0, −2, 2, −2) and **d** = (1, 4, 2, −7) form a basis in R

Is it orthonormal? If the answers are negative, then use the Gram–Schmidt

orthogonalization process to construct an orthonormal basis.

**5.5.** Prove that the set of vectors {(i, 2−i, 5), (1, 2+i, −i), (1, i, −1)} is a basis

in the vector space C3. What are the coordinates of the vectors (1, 0, 0),

(1, 1, 0) and (1, 1, 1) in this basis?

**5.6.** Assume that the vectors **v**1 = [a , a ]T and **v** = [b , b ]T are linearly

1

2

2

1

2

independent. What can you say about the linear dependence or independence

of the vectors **w** = [a , b ]T and **w** = [a , b ]T ?

pq

1

1

1

2

2

2

**5.7.** Prove that the set M = {M } of all matrices with p rows and q columns

with real elements forms a vector space relative to the operations of matrix

addition and matr[ix](#br243)[ ](#br243)[m](#br243)ultiplication b[y](#br243)[ ](#br243)a number.

**5.8.** Prove the **Cauch[y**](#br243)[**7](#br243)–Bunyakovsky[**8](#br243)[ ](#br243)inequality** (also referred to as the

**Cauchy–Schwarz[**9](#br243)[ ](#br243)inequality**):

For arbitrary vectors **x**, **y** ∈ Rn, the following relation is valid:

(**x** · **y**)2  (**x** · **x**)(**y** · **y**),

(5.54)

7Augustin-Louis Cauchy (1789–1857), French mathematician and mechanician.

8Viktor Yakovlevich Bunyakovsky (1804–1889), Russian mathematician and mathematics histo-

rian.

9Karl Hermann Amandus Schwarz (1843–1921), German mathematician.





Problems

233

and the equality is valid if and only if the vectors **x** and **y** differ in the scalar

factor, i.e. are proporti[onal](#br244).

**5.9.** Prove the **Pythagorean[**10](#br244)[ ](#br244)theorem**:

If the vectors **x**, **y** ∈ Rn are orthogonal, then the equality

2

2

2

**x** + **y** = **x** + **y**

(5.55)

(5.56)

is valid.

**5.10.** Check the validity of the identity

2

2

2

2

**x** + **y** + **x** − **y** ≡ 2(**x** + **y** )

for arbitrary elements of the n-dimensional vector space Rn. What is the

R3

geometric sense of this identity in the spaces R and

2

?

**5.11.** It is known that the equalities **x** = 6, **x** + **y** = 10 and **x** − **y** = 12

are valid. What is the variable **x**?

**5.12.** Find the maximum number of linearly independent vectors

(1) on the plane;

(2) in the three-dimensional space;

(3) in Rn.

**5.13.** Check that the system of vectors

[1, 1, 1, . . ., 1]T , [0, 1, 1, . . ., 1]T , [0, 0, 1, . . ., 1]T , . . . , [0, 0, 0, . . . , 1]T

forms a basis in Rn.

**5.14.** Is the system of vectors

2

2

2 T

[1, 1, 1, . . ., 1]T , [1, 2, 3, . . ., n]T , [1, 2 , 3 , . . . , n ] , . . . ,

[1, 2n , 3n−1, . . . , n

−1

n−1 T

]

a basis in Rn?

⎡

⎤

⎡

⎤

0 0

0 a

**5.15.** Show that the matrices ⎣ ⎦ and ⎣ ⎦ , where a ∈ R, are similar.

a 0

0 0

**5.16.** Find whether the matrices A and A are similar:

1

2

⎡

⎤

⎡

⎤

1 −1

0 0

0 0

(1) A = ⎣

⎦ and A = ⎣ ⎦;

1

2

1 1

10Pythagoras of Samos,

Πυθαγόρας ὁ Σάμιος

(about 570 B.C.—about 495 B.C.), Ancient Greek

philosopher and mathematician.





234

5

Vector Spaces

⎡

⎤

⎡

⎤

1 0 0

1 0 1

⎢

⎥

⎢

⎥

(2) A = ⎢0 1 0⎥ and A = ⎢1 0 0⎥.

1

2

⎣

⎦

⎣

⎦

0 0 0

0 1 0

**5.17.** Is it true that the traces of similar matrices coincide?

**5.18.** Find the eigenvalues and eigenvectors of the matrix A.

⎡

⎤

⎡

⎤

4 −5 2

3

1

0

⎢

⎥

⎢

⎥

(1) A = 5 −7 3

⎢

⎥ ; (2)

A

= ⎢

−4 −1 0

4 −8 −2

⎥ ;

(5.57)

(5.58)

(5.59)

⎣

⎡

⎦

⎣

⎦

⎤

6 −9 4

⎤

⎡

2 −1 2

0 1 0

⎢

⎥

⎢

⎥

(3) A = 5 −3 3

⎢

⎥ ;

( ) A

4

= ⎢

−4 4 0

−2 1 2

⎥ ;

⎣

⎦

⎣

⎦

−1 0 −2

⎡

⎤

1 −3 3

⎢

⎥

(5) A = ⎢−2 −6 13⎥ .

⎣

⎦

−1 −4 8

**5.19.** Diagonalize the matrix, i.e. bring the matrix to diagonal form:

⎡

⎤

4 15 −3

⎢

⎥

A = 8 −3

⎢

3

⎥

.

⎣

⎦

0 −15 7

**5.20.** Bring the following matrices to diagonal form:

(1)

⎡

⎤

4

6

1

3

4

6

⎢

⎥

A =

⎢

⎥ ;

⎣

⎦

−11 −5 −11

(2)

⎡

⎤

−23 −16 −28

⎢

⎥

A = 58 39 64

⎢

⎥

.

⎣

⎦

−11 −7 −10





Problems

235

**5.21.** Bring the matrix that depends on the real parameter a to diagonal form:

⎡

⎤

a −1 −1

⎢

⎥

A = −1 a

⎢

1

⎥

.

⎣

⎦

1

1

a

∗**5.22.** Write the characteristic equation for the matrix  of size n × n:

⎡

⎤

0 1 0 . . . 0 0

0 0 1 . . . 0 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

` `= . . . . . . . . . . . . .

⎢

⎥

.

⎢

⎥

⎢

⎥

⎢0 0 0

0 1 ⎥

. . .

⎣

⎦

ω 0 0 . . . 0 0

∗**5.23.** Using the Cayley–Hamilton theorem, compute the n-th power of the matrix

, found in the previous problem.

∗**5.24.** Find the value of the limit:

⎡

⎤

n

1

ϕ/n

lim ⎣

⎦ .

(5.60)

n→∞

−

ϕ/n

1

**5.25.** Bring the complex matrix to diagonal form:

⎡

⎤

1 − 2i 2i 2

⎢

⎥

Z =

⎢

0

i 0

⎥

.

⎣

⎦

i

−2 0

**5.26.** It is known that two out of three eigenvalues of the matrix

⎡

⎤

910

1013 + 57i −1013 + 57i

⎢

⎥

Y = 57 − 899i 68 − 1070i 57 + 1013i

⎢

⎥

⎣

⎦

−57 − 899i 57 − 1013i 68 + 1070i

are equal to 11 + 57i and 11 − 57i. Without solving the characteristic

equation, ﬁnd the third eigenvalue.

**5.27.** Prove that the eigenvalues of Hermitian operator are real.

∗**5.28.** Prove that all eigenvalues of the unitary matrix lie in a complex plane, on a

unit circle with the centre at the origin of coordinates.





236

5 Vector Spaces

**5.29.** Compute the eigenvalues and eigenvectors of the Pauli matrices σ , σ and

1

2

σ3 (see page [185](#br197)).

**Answers and Solutions**

[**5.3**](#br243)[** ](#br243)Solution.

Write the matrix A, composed of the coordinates of the vectors **a**, **b** and **c**:

⎡

⎤

1 −3 0

⎣

⎢

⎥

A = 2 −2 −2

⎢

⎥

.

⎦

3 3 −2

Since det A = 16 = 0, then the vectors are linearly independent and form a

basis. The basis is neither orthogonal, because, for example, (**a** · **b**) = 2 = 0, nor

√

orthonormal, because **a** = 14 = 1.

In order to construct an orthonormal basis, apply the Gram–Schmidt algorithm:

⎡ ⎤

1

⎢ ⎥

1

**t**1

**t**1

**t**1 = **a** =

⎢ ⎥

2

, **q**1

\=

( , , )

= √ 1 2 3 ;

⎣ ⎦

14

3

**t** = **b** − (**b** · **q** )**q**

2

1

1

⎡

⎤

⎡ ⎤

⎡

⎤

−3

1

−11

⎢

⎥

1

1

⎢ ⎥ 2 ⎢

⎥

= ⎢−2⎥ − √ (1 · (−3) + 2 · (−2) + 3 · 3)√ ⎢2⎥ = ⎢ −8 ⎥ ,

⎣

⎦

⎣ ⎦

⎣

⎦

14

14

7

3

3

9

⎡

⎤

−11

−8

9

1

⎢

⎥

**t**2

**q**2 =

= √

266

⎢

⎥ ;

⎣

⎦

**t**2

**t** = **c** − (**c** · **q** )**q** − (**c** · **q** )**q**

3

1

1

2

2

⎡

⎤

⎡ ⎤

0

1

⎢

⎥

1

1

⎢ ⎥

= ⎢−2⎥ − √ (0 · 1 − 2 · 2 − 2 · 3)√ ⎢2⎥

⎣

⎦

⎣ ⎦

14

14

−2

3





Answers and Solutions

237

⎡

⎤

⎡

⎤

−11

3

1

1

⎢

⎥

4 ⎢

⎥

−√

(0 · (−11) − 2 · (−8) − 2 · 9)√

⎢ −8 ⎥ =

⎢−3⎥ ;

⎣

⎦

⎣

⎦

266

266

19

9

1

⎡

⎤

⎥

3

−3

1

1

⎢

**t**3

**q**3 =

= √

19

⎢

⎥

.

⎣

⎦

**t**3

As a result, we obtain the orthonormal basis:

⎡ ⎤

⎡

⎤

⎡

⎤

1

−11

−8

9

3

−3

1

1

⎢ ⎥

1

⎢

⎥

1

⎢

⎥

**q**1 = √

14

⎢ ⎥

2

,

**q**2

= √

⎢

⎥

,

**q**3

= √

⎢

⎥

.

⎣ ⎦

⎣

⎦

⎣

⎦

266

19

3

[**5.4**](#br243)[** ](#br243)Solution.

Write the matrix A, composed of the coordinates of the speciﬁed vectors:

⎡

⎤

3 −3 0

1

⎢

⎥

⎢

⎥

−1 1 −2 4

⎢

⎥

A = ⎢

⎥ .

⎢

⎥

1

0

2

2

⎣

⎦

2 −2 −2 −7

Its determinant is equal to det A = −72 = 0.

It is clear that rk A = 4; then, according to the basic minor theorem, the vectors

**a** = (3, −1, 1, 2), **b** = (−3, 1, 0, −2), **c** = (0, −2, 2, −2) and **d** = (1, 4, 2, −7)

form a basis in the arithmetical space R4.

This basis is neither orthogonal nor orthonormal, because, for example, (**a** · **b**) =

−14 = 0 and (**a** · **a**) = 15 = 1.

In order to construct an orthonormal basis (**q** , **q** , **q** , **q** ), apply the Gram–

1

2

3

4

Schmidt algorithm:

**t**1

**t**1

1

**t**1 = **a** = (3, −1, 1, 2), **q**1 =

**t**2 = **b** − (**b** · **q**1)**q**1

= √ (3, −1, 1, 2);

15

⎡

⎤

⎡

⎤

⎡

⎤

3

3

−3

1 ⎢ 1 ⎥

⎢

⎣

⎥

⎦

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢−1⎥

1

1

⎢−1⎥

= ⎢ ⎥ − √ ((−3) · 3 + 1 · (−1) + 0 · 1 − 2 · 2)√

⎢

⎥ =

⎢

⎥ ,

⎢

⎥

⎢

⎥

⎢

⎥

15

15

15

⎢ 1 ⎥

⎢ 1 ⎥

⎢14⎥

⎣

⎦

⎣

⎦

2

2

−2





238

5

Vector Spaces

⎡

⎤

−3

⎢ 1 ⎥

⎢

⎥

⎢

⎥

**t**2

**t**2

1

**q**2 =

= √

⎢

⎥ ;

⎢

⎥

210

⎢14⎥

⎣

⎦

−2

⎡

⎤

⎡

⎤

⎡

⎤

0

−3

3

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢−2⎥

1 ⎢ 1 ⎥ 1 ⎢−15⎥

**t**3 = **c** − (**c** · **q**1)**q**1 − (**c** · **q**2)**q**2 =

⎢

⎥ − 0 ·

**q**1

−

⎢

⎥ =

⎢

⎥

,

⎢

⎥

⎢

⎥

⎢

⎥

7

7

⎢ 2 ⎥

⎢14⎥

⎢ 0 ⎥

⎣

⎦

⎣

⎦

⎣

⎦

−2

−2

−12

⎡

⎤

1

⎢

⎥

⎢

⎥

1

⎢−5⎥

**t**3

**t**3

**q**3 =

= √

42

⎢

⎥ ;

⎢

⎥

⎢ 0 ⎥

⎣

⎦

4

**t**4 = **d** − (**d** · **q**1)**q**1 − (**d** · **q**2)**q**2 − (**d** · **q**3)**q**3

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

⎡

⎤

1

1

−3

3

4

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢ 4 ⎥

3

⎢−5⎥

43 ⎢ 1 ⎥ 13 ⎢−1⎥ ⎢ 4 ⎥

= ⎢ ⎥ −

⎢

⎥ −

⎢

⎥ +

⎢

⎥ = ⎢ ⎥ ,

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

124

210

15

⎢ 2 ⎥

⎢ 0 ⎥

⎢14⎥

⎢ 1 ⎥ ⎢ 0 ⎥

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

⎣

⎦

−7

−4

−2

2

−4

⎡

⎤

1

⎢

⎥

⎢

⎥

1

⎢ 1 ⎥

**t**4

**t**4

**q**4 =

= √

⎢

⎥

.

⎢

⎥

3

⎢ 0 ⎥

⎣

⎦

−1

As a result, enumerate the vectors of the orthonormal basis:

⎡

⎤

⎡

⎤

3

−3

⎢

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

−1

1

1

⎢

⎥

⎥

**q**1 = √

⎥ , **q**2 = √

⎢

⎢

⎥ ,

15 ⎢ 1 ⎥

210 ⎢14⎥

⎣

⎦

⎣

⎦

2

−2





Answers and Solutions

239

⎡

⎤

⎡

⎤

1

4

4

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

1

−5

1

⎢

⎥

⎢

⎥

**q**3 = √

⎥ , **q**4 = √ ⎢ ⎥ .

⎢

42 ⎢ 0 ⎥

4 3 ⎢ 0 ⎥

⎣

⎦

⎣

⎦

−4

−4

[**5.5**](#br243)[** ](#br243)Solution.

Construct a matrix A of the coordinates of the speciﬁed vectors:

⎡

⎤

i

1

1

⎢

⎥

A = 2 − i 2 + i i

⎢

⎥

.

⎣

⎦

5

−i −1

Its determinant is det A = −8 − 6i = 0, and therefore, the set of vectors forms a

basis in the space C3.

Find the coordinates of the vectors **a** = (1, 0, 0), **b** = (1, 1, 0) and **c** = (1, 1, 1)

in this basis.

The vector **a** in the basis (**e** , **e** , **e** ) has the coordinates (a , a , a ) that satisfy

1

2

3

1

2

3

the system of equations, which in matrix notation has the form:

⎡

⎤ ⎡

⎤

⎡ ⎤

i

1

1

a1

1

⎢

⎥ ⎢

⎥

⎢ ⎥

⎢

⎥ ⎢ ⎥ = ⎢ ⎥

2 − i 2 + i i

5

a

0

.

⎣

⎦ ⎣ 2⎦ ⎣ ⎦

−i −1

a

0

3

In order to solve the obtained system, let us use Cramer’s rule, according to

i

which, for i ∈ {1, 2, 3}, the equalities ai =

are valid.

` `= −8 − 6i,




1

1

1




1 = 0 2 + i i

` `= −3 −

i,




0 − −1

i




1 1

` `i



2 = 2 − i 0 i

` `= 2 + 4

i,




` `5 0 −1





240

5 Vector Spaces




1

1

` `i



3 = 2 − i 2 + i 0

` `= −11 − 7

i.




` `5

−

0

i

Hence, we obtain the following coordinates:

−3 − i

1

1

**a** = (a , a , a ), where a =

\=

(3 − i), a2 = − (4 + 2i) and

10 10

1

2

3

1

−8 − 6i

1

a3 =

(13 − i).

10

Write the system of equations for the coordinates of the second vector **b**:

⎡

⎤ ⎡

⎤

⎡ ⎤

i

1

1

b1

1

⎢

⎥ ⎢

⎥

⎢ ⎥

⎢

⎥ ⎢ ⎥ = ⎢ ⎥

2 − i 2 + i i

5

b

1

.

⎣

⎦ ⎣ 2⎦ ⎣ ⎦

−i −1

b

0

3




1

1

1




1 = 1 2 + i i

` `= −2 − 2

i,

i,




0 − −1

i




1 1

` `i



2 = 2 − i 1 i

` `= −3 + 3




` `5 0 −1




1

1

` `i



3 = 2 − i 2 + i 1

` `= −7 − 7

i.




` `5

−

0

i

1

1

The values of the coordinates are b1

\=

(7 + i), b2

\=

(3 − 21i) and

50

25

1

b3 =

(49 + 7i).

50

Finally, the coordinates of the vector **c** satisfy the following system of equations

in matrix form:

⎡

⎤ ⎡

⎤

⎡ ⎤

i

1

1

a1

1

⎢

⎥ ⎢

⎥

⎢ ⎥

⎢

⎥ ⎢ ⎥ = ⎢ ⎥

2 − i 2 + i i

5

a

1

.

⎣

⎦ ⎣ 2⎦ ⎣ ⎦

−i −1

a

1

3





Answers and Solutions

241




1

1

1




1 = 1 2 + i i

` `= −4 − 2

i,




1 − −1

i




1 1

` `i



2 = 2 − i 1 i

` `= 2

i,




` `5 1 −1




1

1

` `i



3 = 2 − i 2 + i 1

` `= −10 − 4

i.




` `5

−

1

i

1

1

The coordinates of the vector **c** are equal to c =

(11−2i), c2 = − (3+4i)

1

25

25

1

and c3 =

(26 − 7i).

25

[**5.6**](#br243)[** ](#br243)Solution.

The criterion, i.e. the necessary and sufﬁcient condition of the linear indepen-

dence of the system of vectors **v** and **v** is the determinant being not equal to zero,

1

2

which determinant is composed of their coordinates:






a1 b1

` `= 0

.


a b 

2

2

As is known, transposition of a matrix does not change its determinant. There-

fore, there exists the inequality






a1 a2

` `= 0

,


b b 

1

2

and the vectors **w** = [a , b ]T and **w** = [a , b ]T are independent.

1

1

1

2

2

2

[**5.7**](#br243)[** ](#br243)Proof.

Each matrix from the set M can be presented as a numerical sequence of length

p × q. Indeed, for this, it is enough to write the matrix elements row by row into a

vector, or, in other words, into a one-dimensional array of size p × q. Since the

vectors of the same size form an arithmetical space, then the set M = {M

}

pq

also forms a vector space relative to the operations of matrix addition and matrix

multiplication by a number.





242

5 Vector Spaces

[**5.8**](#br243)[** ](#br243)Proof.

Let us introduce for consideration the vector **z** = **x** − λ**y**, where λ is some real

number.

Based on the fourth property of scalar product, (**z**, **z**)  0, or

((**x** − λ**y**) · (**x** − λ**y**)) = (**x** · **x**) − 2λ(**x** · **y**) + λ2(**y** · **y**) 0.

(5.61)

This inequality should be valid for any λ ∈ R. Note that the left side of the

inequality ([5.61](#br253)) is a quadratic trinomial. The necessary and sufﬁcient condition of

its non-negativity is non-positivity of the discriminant:

(**x** · **y**)2 − (**x** · **x**)(**y** · **y**) 0.

The obtained inequality, as it is easy to see, after transferring the summand (**x** ·

**x**)(**y** · **y**) to the right side, coincides with the Cauchy–Bunyakovsky inequality.

The equals sign will occur if and only if **z** ≡ 0, i.e. **x** and **y** are proportional and

differ in the scalar factor.

[**5.9**](#br244)[** ](#br244)Proof.

From the deﬁnition of vector length and the properties of scalar product, follow

the equalities

2

2

2

**x** +**y** = ((**x** +**y**)·(**x** +**y**)) = (**x** ·**x**)+(**x** ·**y**)+(**y** ·**x**)+(**y** ·**y**) = **x** +**y** .

Thus, the Pythagorean theorem is proved for all orthogonal vectors **x**, **y** ∈ Rn.

[**5.10**](#br244)[** ](#br244)Solution.

Transforming the squares of norms in the left side of the identity, we obtain

2

2

2

**x** + **y** = ((**x** + **y**) · (**x** + **y**)) = **x** + 2(**x** · **y**) + **y** ,

(5.62)

(5.63)

2

2

2

**x** − **y** = ((**x** − **y**) · (**x** − **y**)) = **x** − 2(**x** · **y**) + **y** .

From these relations, follow the equality ([5.56](#br244)). The geometric sense of this equality

consists in that the sum of the squares of the parallelogram’s diagonals is equal to

the sum of the squares of the sides.

[**5.11**](#br244)[** ](#br244)Solution.

Express the variable **y**, using the identity ([5.56](#br244)) from the previous problem:

\+

**y** = (**x** + **y**2 + **x** − **y**2)/2 − **x**2.

√

Having substituted the numeric data, we obtain **y** = (100 + 144)/2 − 36 =

√

\86.





Answers and Solutions

243

[**5.12**](#br244)[** ](#br244)Answer.

(1) The maximum number of linearly independent vectors equals to 2;

(2) 3;

(3) n.

[**5.13**](#br244)[** ](#br244)Solution.

The matrix of the system of vectors under consideration has a lower triangular

⎡

⎤

1 0 . . . 0 0

1 1 . . . 0 0

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

form: ⎢ . . . . . . . . . . . ⎥

⎢

⎥

⎢

⎥

⎢1 1

1 0 ⎥

. . .

⎣

⎦

1 1 . . . 1 1

Its determinant is equal to the product of the elements located on the main

diagonal. Therefore, the vectors are linearly independent and form a basis in the

vector space Rn.

[**5.14**](#br244)[** ](#br244)Answer: It is. This is easily seen from the Vandermonde determinant being not

equal to zero in this case (see ([2.74](#br81)) on page [67](#br81)).

[**5.15**](#br244)[** ](#br244)Solution.

It is easy to verify that the equality is valid:

⎡

⎤

⎡

⎤

⎦

0 a

0 0

⎣

⎦ = −1 ⎣

P

P,

0 0

a 0

⎡

⎤

0 1

where P = ⎣ ⎦. Therefore, by deﬁnition of similarity relation ([5.27](#br236)), the

1 0

matrices mentioned in the statement of the problem are similar.

[**5.16**](#br244)[** ](#br244)Answer:

⎡

⎤

⎦

⎡

⎤

−1

0 1

0 1

(1) Yes, A = ⎣

A ⎣

⎦;

2

1

−1 0

−1 0

(2) No, since the equality of the determinants of these matrices is not fulﬁlled.

[**5.17**](#br245)[** ](#br245)Solution.

Yes, as follows from Problem [**1.44**](#br46), for any matrices A and the invertible matrix

P, the equality

tr (P−1AP) = tr (AP−1P) = tr A

is fulﬁlled.





244

5 Vector Spaces

[**5.18**](#br245)[** ](#br245)Solution.

(1) As is known, the eigenvector of the matrix A is such vector **u**, in which

multiplication of A by **u** results in the vector λ**u**, where λ ∈ R is the eigenvalue.

Write an equation of the form A**u** = λ**u**:

⎡

⎤ ⎡

⎤

⎡

⎤

4 −5 2

5 −7 3

6 −9 4

u1

u1

u

⎢

⎥ ⎢

⎥

⎢

⎥

⎢

⎥ ⎢ ⎥ =

⎢

⎥

u

λ

⎣ 2⎦

,

⎣

⎦ ⎣ 2⎦

u

3

u

3

or in the coordinates of the vector **u**:

⎧

⎪4 − 5 + 2

\=

⎪ u

u2

u3 λu1,

⎨

1

5u − 7u + 3u = λu ,

1

2

3

2

⎪

⎪

⎩

6u − 9u + 4u = λu ,

1

2

3

3

⎧

⎪

⎪(4 − λ)u − 5u + 2u = 0,

⎨

1

2

3

5u − (7 + λ)u + 3u = 0,

1

2

3

⎪

⎪

⎩

6u − 9u + (4 − λ)u = 0.

1

2

3

Note that the eigenvector cannot be zero by deﬁnition:

⎡

⎤

⎡ ⎤

u1

u2

u3

0

⎢

⎥

⎢ ⎥

⎢

⎥ = ⎢ ⎥

0

.

⎣

⎦

⎣ ⎦

0

Therefore, the equations are linearly dependent and the determinant of the

system matrix is equal to zero:




4 − λ)

5u2

2u3

(




` `= 0

5u1 −(7 + λ)u2

3u3

.




` `6

−9u2

4 −

u1

(

λ)u3

Having computed the determinant, we obtain the characteristic equation:

λ

2 − 3 = 0.

λ

The eigenvalues are λ1,2 = 0 and λ3 = 1, so zero is an eigenvalue of

multiplicity two.





Answers and Solutions

245

Find the respective eigenvectors:

Let λ = 0.

⎧

⎪

⎪4u − 5u + 2u = 0,

⎨

1

2

3

5u − 7u + 3u = 0,

1

2

3

⎪

⎪

⎩

6u − 9u + 4u = 0.

1

2

3

Having solved this system, we obtain

⎡

⎤

⎡

⎤

u1

u1

⎢

⎥

⎢

⎥

u1 = 0, u2 = 2u1, u3 = 3u1, or

⎢

⎥ = ⎢

2u , u1

⎥

∈ R

.

⎣ 2⎦

u

⎣

1⎦

u3

3u1

⎡ ⎤

1

⎢ ⎥

The eigenvector is ⎢2⎥.

⎣ ⎦

3

Let λ = 1.

⎧

⎪3 − 5 + 2 = 0

⎪ u

u2

u3

,

⎨

1

5u − 8u + 3u = 0,

1

2

3

⎪

⎪

⎩

6u − 9u + 3u = 0.

1

2

3

Having solved this system, we obtain

⎡

⎤

⎡

⎤

u1

u2

⎢

⎥

⎢

⎥

u1 = u2, 0u2 = 0u2, u3 = u2 or

⎢

⎥ = ⎢ ⎥,

u2

∈ R. The eigenvector

⎣ 2⎦

u

⎣ 2⎦

u

u3

u2

⎡ ⎤

1

⎢ ⎥

is ⎢1⎥.

⎣ ⎦

1

(2) By analogy with the solution from the previous item, write an equation of the

form A**u** = λ**u**. Then, we obtain the characteristic equation:

−(λ + 2)(λ − 1)2 = 0.

The eigenvalues are equal to λ1 = −2 and λ2,3 = 1.





246

5 Vector Spaces

Let us ﬁnd the eigenvectors.

For λ = −2,

⎧

⎪5

\+

1

= 0

2

⎪ u

u2

,

⎨

1

−4u + u = 0,

⎪

⎪

⎩

4u − 8u = 0,

1

2

u1 = 0, u2 = 0, u3 ∈ R.

⎡ ⎤

0

⎢ ⎥

The eigenvector is ⎢0⎥.

⎣ ⎦

1

For λ = 1,

2,3

⎧

⎪2

\+

1

= 0

2

⎪ u

u2

,

⎨

1

−4u − 2u = 0,

⎪

⎪

⎩

4u − 8u − 3u = 0,

1

2

3

20

u2 = −2u1, u3 =

u1,

3

⎡

⎤

⎡

⎤

u1

u1

u2

u3

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥ = −2

∈ R

⎢

u1⎥ , u

.

1

⎣

⎦

⎣

⎦

20

u1

3

⎡

⎤

3

⎢

⎥

The eigenvector is ⎢−6⎥.

⎣

⎦

20

3

2

(3) The characteristic equation: −λ − 3λ − 3λ − 1 = 0.

The eigenvalue is multiple of three: λ = −1.

⎧

⎪

⎪3u − u + 2u = 0,

⎨

1

2

3

5u − 2u + 3u = 0,

1

2

3

⎪

⎪

⎩

−u − u = 0.

1

3





Answers and Solutions

247

Find non-trivial solutions: u = −u and u = −u .

1

3

2

3

⎡

⎤

−1

⎢

⎥

The eigenvector is ⎢−1⎥.

⎣

⎦

1

(4) The characteristic equation has the form: −(λ − 2)3 = 0.

The eigenvalue is λ = 2.

Find the eigenvector for λ = 2:

⎧

⎪

⎪−2u + u = 0,

⎨

1

2

−4u + 2u = 0,

1

2

⎪

⎪

⎩

−2u + u = 0,

1

2

then **u** = c [1/2, 1, 0]T + c [0, 0, 1]T .

1

2

The eigenvectors: [1, 2, 0]T , [0, 0, 1]T .

3

2

(5) The characteristic equation: −λ + 3λ − 3λ + 1 = 0.

The eigenvalue λ = 1 is multiple of three.

⎧

⎪

⎪−3u + 3u = 0,

⎨

2

3

−2u − 7u + 13u = 0,

1

2

3

⎪

⎪

⎩

−u − 4u + 7u = 0,

1

2

3

and therefore, u = u and u = 3u .

2

3

1

3

⎡

⎤

3u3

⎢

⎥

⎢

⎥

∈ R

u3 , u3

.

⎣

⎦

u3

⎡ ⎤

3

⎢ ⎥

The eigenvector is ⎢1⎥.

⎣ ⎦

1

[**5.19**](#br245)[** ](#br245)Solution.

Compose the characteristic equation:

⎡

⎤

4 − λ 15

−3

⎢

⎥

det ⎢

⎥ = 0.

8

−3 −

λ

3

⎣

⎦

0

−15 7 − λ





248

5 Vector Spaces

Find the characteristic polynomial, expanding the determinant in the ﬁrst column:

p(λ) = (4 − λ)((−3 − λ)(7 − λ) + 45) − 8(15(7 − λ) − 45),

3

2

p(λ) = λ − 8λ − 80λ + 384.

Find the eigenvalues: λ = 12, λ = −8 and λ = 4.

1

2

3

Compose the eigenvectors.

⎧

⎪−8 + 15 − 3 = 0

⎪

x1

x2

x3

,

⎨

(1) For λ1,

(2) For λ2,

8

− 15 + 3 = 0

⇒ **a**1 = c(3, 1, −3).

x1

x2

x3

,

⎪

⎪

⎩

−15x − 5x = 0

2

3

⎧

⎪12 + 15 − 3 = 0

⎪

x1

x2

x3

,

⎨

8x + 5x + 3x = 0,

⇒ **a**2 = c(−1, 1, 1).

1

2

3

⎪

⎪

⎩

−15x + 15x = 0

2

3

(3) For λ3,

⎧

⎪15 − 3 = 0

⎪

x2

x3

,

⎨

8x − 7x + 3x = 0, ⇒ **a**3 = c(−1, 1, 5).

1

2

3

⎪

⎪

⎩

−15x + 3x = 0

2

3

Write the transformation matrix and the matrix inverse of it:

⎡

⎤

⎡

⎤

3 −1 −1

1 1 0

−2 3 −1

1 0 1

⎢

⎥

1 ⎢

⎥

P =

⎢

1

1

1

⎥

,

P

−1 =

⎢

⎥

.

⎣

⎦

⎣

⎦

4

−3 1

5

As a result, the diagonalized matrix is equal to

⎡

⎤

⎡

⎤

12 0 0

−3 −1 −1

⎢

⎥

⎢

⎥

B = P−1AP = 0 −8 0 , where P = −1 1

⎢

⎥

⎢

⎥

.

1

⎣

⎦

⎣

⎦

0

0 4

3

1

5





Answers and Solutions

249

[**5.20**](#br245)[** ](#br245)Solution.

(1) The characteristic equation has the form:

⎡

⎤

4 − λ

⎣

1

4

6

⎢

⎥

|A − λI| = ⎢

⎥ = 0.

6

3 −

λ

⎦

−11 −5 −11 − λ

Compute the characteristic polynomial:

p(λ) = (4 − λ)((3 − λ)(−11 − λ) + 30) − (6(−11 − λ) + 30)

+4(−30 − (3 − λ) · (−11)),

3

2

p(λ) = −λ − 4λ − 3λ.

The eigenvalues are λ = −3, λ = −1 and λ = 0.

1

2

3

Compose the eigenvectors.

For λ1,

⎧

⎪

⎪7x + x + 4x = 0,

⎨

1

2

3

6x + 6x + 6x = 0,

⇒ **a**1 = c(1, 1, −2).

1

2

3

⎪

⎪

⎩

−11x − 5x − 8x = 0

1

2

3

For λ2,

⎧

⎪

⎪5x + x + 4x = 0,

⎨

1

2

3

6x + 4x + 6x = 0,

⇒ **a**2 = c(5, 3, −7).

⇒ **a**3 = c(−1, 0, 1).

1

2

3

⎪

⎪

⎩

−11x − 5x − 10x = 0

1

2

3

⎧

⎪4

\+

x3

\+ 4 = 0

⎪ x

x2

,

⎨

1

For λ3,

6

\+ 3 + 6 = 0

x1

x2

x3

,

⎪

⎪

⎩

−11x − 5x − 11x = 0

1

2

3

⎡

⎤

1

5 −1

⎢

⎥

The transformation matrix is P = ⎢ 1

0 ⎥,

3

⎣

⎦

−2 −7 1

⎡

⎤

−3 −2 −3

⎢

⎥

the matrix inverse of it has the form P−1 = ⎢ 1

1 ⎥.

1

⎣

⎦

1

3

2





250

5 Vector Spaces

The diagonalized matrix:

⎡

⎤

⎡

⎤

−3 0 0

1

1

5 −1

⎢

⎥

⎢

⎥

B = P−1AP = 0 −1 0 , where P =

⎢

⎥

⎢

⎥

.

3

0

⎣

⎦

⎣

⎦

0

0 0

−2 −7 1

(2) Write the characteristic equation:

⎡

⎤

−23 − λ −16

−28

⎢

⎥

A − λI =

⎢

58

39 − λ

64

⎥ = 0

,

⎣

⎦

−11

−7 −10 − λ

p(λ) = (−23 − λ)((39 − λ)(−10 − λ) + 64 · 7) + 16(58(−10 − λ)

+11 · 64) − 28(−7 · 58 + 11(39 − λ)),

3

2

p(λ) = −λ + 6λ − 11λ + 6.

The eigenvalues are λ = 3, λ = 2 and λ = 1.

1

2

3

Compose the eigenvectors.

For λ1,

⎧

⎪

⎪−26x − 16x − 28x = 0,

⎨

1

2

3

58x + 36x + 64x = 0,

⇒ **a**1 = c(2, −5, 1).

⇒ **a**2 = c(4, −8, 1).

⇒ **a**3 = c(5, −11, 2).

1

2

3

⎪

⎪

⎩

−11x − 7x − 13x = 0

1

2

3

For λ2,

⎧

⎪−25 − 16 − 28 = 0

⎪

x1

x2

x3

,

⎨

58x + 37x + 64x = 0,

1

2

3

⎪

⎪

⎩

−11x − 7x − 12x = 0

1

2

3

For λ3,

⎧

⎪

⎪−24x − 16x − 28x = 0,

⎨

1

2

3

58x + 38x + 64x = 0,

1

2

3

⎪

⎪

⎩

−11x − 7x − 11x = 0

1

2

3

⎡

⎤

2

4

5

⎢

⎥

The transformation matrix is P = ⎢−5 −8 −11⎥,

⎣

⎦

1

1

2





Answers and Solutions

251

⎡

⎤

−5 −3 −4

⎢

⎥

and the matrix inverse of it is P−1 = ⎢−1 −1 −3⎥.

⎣

⎦

3

2

4

Write the diagonalized matrix:

⎡

⎤

⎡

⎤

3 0 0

2

4

5

⎢

⎥

⎢

⎥

B = P−1AP = 0 2 0 , where P = −5 −8 −11

⎢

⎥

⎢

⎥

.

⎣

⎦

⎣

⎦

0 0 1

1

1

2

[**5.21**](#br246)[** ](#br246)Answer:

The characteristic polynomial has the form p(λ) = λ3 −3aλ2 +3a2λ−λ+(a−

a )

3 ; its roots are equal to

λ1

\=

a

− 1,

λ2

\=

a

and

λ3

\=

a

\+ 1.

The diagonalized matrix is equal to

⎡

⎤

⎡

⎤

a + 1 0

0

0

−1 1

0

⎢

⎥

⎢

⎥

B = P−1AP =

⎢

⎥

, where P = 1 −1 −1

⎢

⎥

.

0

a

⎣

⎦

⎣

⎦

0

0 a − 1

0

1

1

[**5.22**](#br246)[** ](#br246)Solution.

Write the left side of the characteristic equation det( − λI) = 0, expanding the

determinant in the ﬁrst column:




−λ 1 0 . . . 0

0

0





0 −λ 1 . . . 0




det( − λI) =  . . . . . . . . . . . . . . . . . . . . . . 




` `0 0 0

−

1

. . .

. . .

λ





0 0

0

−

ω

λ








−λ 1 0 . . . 0 

` `1 0 . . . 0 0 








0 −λ 1 . . . 0

−λ 1 . . . 0

0








=  . . . . . . . . . . . . . . .  − (−1)n  . . . . . . . . . . . . . . . 








` `0 0 0

1 

` `0 0

1

0 

. . .

. . .

. . .

. . .









0 0

− 

` `0 0

−

1 

ω

λ

λ

−1

n

n

n

= − λ(−λ)n − (−1) ω = (−λ) − (−1) ω.

As a result, the characteristic equation for the matrix  has the form (−1)n(λn −

ω) = 0 or (λn −

ω)

= 0.





252

5 Vector Spaces

[**5.23**](#br246)[** ](#br246)Solution.

According to the Cayley–Hamilton theorem, when the matrix is substituted into

its characteristic equation, an identity is obtained. As is shown in Problem [**5.22**](#br246), the

characteristic equation for  has the form (λn − ω) = 0. Then, the equality is valid:

n − ωI O, or n = ωI,

\=

where, as usual, O is the zero matrix of size n × n and I is the identity matrix of the

same size.

[**5.24**](#br246)[** ](#br246)Solution.

⎡

⎤

1

ϕ/n

Denote A = ⎣

⎦.

−ϕ/n 1

The eigenvalues of this matrix are equal to λ = 1 ± iϕ/n; the eigenvectors

1,2

corresponding to them are equal to [1, i]T and [1, −i]T .

Compute the power of An, having brought the matrix to diagonal form A ﬁrst:

⎡

⎤

⎡

⎤ ⎡

⎤

⎡

⎤

−1

1 1

1

ϕ/n

1 1

1 + iϕ/n

0

A =

⎣

⎦

⎣

⎦ ⎣

⎦

\=

⎣

⎦

,

i −i

−ϕ/n 1

i −i

0

1 − iϕ/n

and therefore, according to the theorem on the power of a special form matrix on

page [56](#br70),

⎡

⎤

⎡

⎤

1 1

1 1

n = ⎣

⎦

(A )

` `n ⎣

⎦

A

i −i

i −i

⎡

⎤

⎦

⎡

⎤ ⎡

⎦ ⎣

⎤

⎦

−1

−1

1 1

(1 + iϕ/n)n

0

1 1

= ⎣

⎣

.

i −i

0

(1 − iϕ/n)n

i

−

i

After simple computations, we obtain

⎡

⎤

⎦

1

2

(1 + iϕ/n)n + (1 − iϕ/n)n i(−(1 + iϕ/n)n + (1 − iϕ/n)n)

An =

⎣

.

i((1 + iϕ/n)n − 1 −

(

n

iϕ/n) )

(

1 +

iϕ/n)

n + 1 −

(

iϕ/n)

n

Using the relation known from mathematical analysis [[76](#br422)[\]](#br422)

lim (1 + t/n)n = et ,

n→∞





Answers and Solutions

253

which is valid for all t ∈ C, perform the limit operation:

⎡

⎤

1

2

iϕ/n +

e

−iϕ/n

−

i(eiϕ/n − e−iϕ/n

)

e

lim An =

⎣

⎦ .

n→∞

−iϕ/n −

eiϕ/n

−

iϕ/n

−

i(e

)

eiϕ/n +

e

Representing the exponent of the imaginary number by Euler’s formula cos z +

i sin z = e

iz, we arrive at the ﬁnal answer:

⎡

⎤

⎡

⎤

n

1

ϕ/n

cos ϕ sin ϕ

− sin cos

lim ⎣

⎦ = ⎣

⎦ .

n→∞

−

ϕ/n

1

ϕ

ϕ

[**5.25**](#br246)[** ](#br246)Answer:

⎡

⎤

⎡

⎤

−2i 0 0

−2 −2i −i

⎢

⎥

⎢

⎥

Z = P−1ZP =

⎢

⎥

⎢

⎥

.

0

i 0 , where P = 0 1 − i 0

⎣

⎦

⎣

⎦

0 0 1

1

2

1

[**5.26**](#br246)[** ](#br246)Solution.

As is known, the traces of identical matrices coincide (see Problem [**5.17**](#br245)[**).](#br245)

Therefore, the sum of the eigenvalues of the matrix is equal to the trace of this

matrix:

3

tr Y = λ + λ + λ =

yii = 910 + (68 − 1070i) + (68 + 1070i) = 1046,

1

2

3

i=1

and the third eigenvalue is equal to

λ3 = 1046 − (λ1 + λ2) = 1046 − ((11 + 57i) + (11 − 57i)) = 1024.

[**5.27**](#br246)[** ](#br246)Proof.

Let A be an arbitrary Hermitian matrix of size n × n that has the eigenvector **b**,

which is satisﬁed by the eigenvalue λ . This means that the equality is fulﬁlled

0

A**b** = λ0**b**.

(5.64)

Consider the expression **b**H A**b**. It is equal to a real number, since according to

the theorem on Hermitian conjugation of product on page [181](#br193),

(**b**H A**b**)H =

H

**b** A (**b** )

H

H

H =

**b**H A**b**.

(5.65)





254

5

Vector Spaces

According to ([5.64](#br264)), the equality is fulﬁlled

λ **b b** λ ( b1|2 + |b2|2 + · · · + |b |2),

\=

|

(5.66)

**b**H A**b**

\=

H

0

0

n

where b , b , . . . , b are the components of the vector **b**.

1

2

n

Comparing ([5.65](#br264)) and ([5.66](#br265)), we obtain that λ0 ∈ R.

[**5.28**](#br246)[** ](#br246)Proof.

Let U be an arbitrary unitary matrix that has the eigenvector **b**, which is satisﬁed

by the eigenvalue λ0. This means that the equality is fulﬁlled

U**b** = λ0**b**.

(5.67)

Consider the expression (U**b**)H (U**b**). By virtue of ([5.67](#br265)), this expression can be

presented in the form:

\=

(λ0**b**)H (λ0**b**) (λ **b** )(λ0**b**) λ λ0**b b**

\=

\=

= |λ0|2

(5.68)

(U**b**)H (U**b**)

∗

H

∗

0

H

H

**b b**.

0

Note that the transformations used property (3) of the Hermitian conjugate operation

(see page [181](#br193)).

On the other hand, relying on the theorem on Hermitian conjugation of product

on page [181](#br193)[ ](#br193)and on the property of unitarity of UH U = I, we obtain

(U**b**)H (U**b**)

\=

H

H

\=

H

H

\=

H

\=

H

(**b** U )(U**b**) **b** (U U)**b b** I**b b b**.

(5.69)

Comparing ([5.68](#br265)) and ([5.69](#br265)), we come to the conclusion: |λ |2 = 1.

0

Therefore, the complex number λ is located on a complex plane, at a distance

0

of ρ = 1 from the origin of coordinates. The locus of all such points λ is the unit

0

circle with the centre at the origin of coordinates, which is what we set out to prove.

[**5.29**](#br247)[** ](#br247)Answer:

⎡

⎡

⎤

⎤

1

1

for σ1, λ1,2 = ± 1, the eigenvectors are **b**1,2 = √ ⎣ ⎦;

for σ2, λ1,2 = ± 1, the eigenvectors are **b**1,2 = √ ⎣ ⎦;

for σ3, λ1,2 = ± 1, the eigenvectors are **b** = ⎣ ⎦ and **b** = ⎣ ⎦.

2

± 1

1

1

2

±

i

⎡ ⎤

⎡ ⎤

1

0

1

2

0

1





**Chapter 6**

**Vectors in a Three-Dimensional Space**

−→

**Geometrical vector** is a directed segment AB with the beginning at the point A and

the end at the point B. Hereinafter, the word “geometrical” in this deﬁnition will be

omitted for brevity.

**Zero vector**, or **null vector**, is a vector whose beginning and end coincide.

The length of the segment AB is called the modulus or **magnitude** of the vector

−→

−→

AB and is denoted by |AB|.

The vectors lying on parallel lines are referred to as **collinear**.

**Unit vector** is a vector whose modulus is equal to one.

The vector **b** is the product of the number α and the vector **a**, if the following

conditions are met:

(1) |**b**| = abs(α)|**a**|;

(2) directions of the vectors **a** and **b** coincide if α > 0, and these vectors are

oppositely directed if α < 0.

The product of zero and **a** is equal to zero vector by deﬁnition.

−→

−→

The two vectors AB and CD are considered to be **equal**, and if they are collinear,

they have the same moduli and are unidirectional.

A vector

−→

AB

**ε** = −→

(6.1)

|AB|

−→

is called the **normalized vector** of the vector AB. It is a unit vector whose direction

−→

coincides with that of the vector AB.

When determining the **sum** of vectors, the law of parallelogram should be used

(see Fig. [6.1](#br267)).

© Springer Nature Switzerland AG 2021

255

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_6>





256

6

Vectors in a Three-Dimensional Space

**Fig. 6.1** Determine the

vector **c** as the sums of the

vectors **a** and **b** (law of

parallelogram)

**a**

**c** = **a** + **b**

**b**

Let the line L and the point A be speciﬁed in the space. Let us draw, through the

point A, the plane π, which is orthogonal to the line L. The point of intersection of

the plane π and the line L is called the **projection** of the point A on the line L.

−→

Consider the vector AB and the line L in space. Let A and B be projections

−−→

of the points A and B on the line L, respectively. Then, the vector AB is called a

−→ −→

**projection** of the vector AB on the line L and is denoted by Pr AB.

L

−→

The **numeric projection** of the vector AB on the line L is equal to the modulus

−→ −→

|AB|, multiplied by the cosine of the angle α between the vector AB and the line L,

−→ −→

i.e. Pr AB = |AB| cos α.

L

Numeric projections of vectors have the following properties:

Pr (**a** + **b**) = Pr **a** + Pr **b**,

(6.2)

(6.3)

L

L

L

Pr (α**a**) = αPr **a**.

L

L

**6.1 Cartesian Coordinate System**

Cartesian[1](#br267)[ ](#br267)coordinate system is a system that consists of the reference point O, the

mutually perpendicular axes Ox, Oy, Oz, that intersect at the point O, and a scale

unit segment.

−→

Let A be an arbitrary point in space. The vector OA is called a **position vector**

−→

of the point A. The numeric projection of the vector OA on the axis Ox is denoted

by x and is called an **abscissa**, on the axis Oy by y and is [called](#br420)[ ](#br420)[an](#br421)[ ](#br421)**ordinate**, and

on the axis Oz by z and is called an **applicate** of the point A [[19](#br420)[,](#br420)[ ](#br420)[23](#br421)[\].](#br421)

The respective coordinates of the equal vectors coincide.

1René Descartes (1596–1650), French philosopher, mathematician, physicist and physiologist.





6.1 Cartesian Coordinate System

257

**Fig. 6.2** Cartesian

coordinate system

z

A

**k**

**j**

y

O

**i**

x

The real numbers x, y, z are coordinates of the point A and the position vector

−→ −→

OA, which can be written as A(x, y, z) and OA = (x, y, z).

**Normalized vectors (basis vectors)** of Cartesian coordinate system are the unit

vectors **i**, **j**, **k** (see Fig. [6.2](#br268)). In coordinate representation, they have the following

form: **i** = (1, 0, 0), **j** = (0, 1, 0) and **k** = (0, 0, 1).

−→

An arbitrary vector AB = (x, y, z) can be represented in the form of a **basis**

**expansion** of Cartesian coordinate system:

−→

AB = x**i** + y**j** + z**k**.

(6.4)

The linear operations on vectors, i.e. addition of vectors and multiplication of a

vector by a number, are said to be performed component-wise or coordinate-wise.

This means that if **a** = (a , a , a ), **b** = (b , b , b ) and c ∈ R, then

x

y

z

x

y

z

**a** + **b** = (a + b , a + b , a + b ), c**a** = (ca , ca , ca ).

(6.5)

x

x

y

y

z

z

x

y

z

With the help of the normalized vectors of the coordinate system, the obtained

equalities can be written as

**a**+**b** = (a +b )**i**+(a +b )**j** +(a +b )**k**, c**a** = ca **i**+ca **j** +ca **k**.

(6.6)

x

x

y

y

z

z

x

y

z

Let us illustrate the use of the introduced deﬁnitions by the following example.

Example 6.1 For the vectors **v**1 = (−2, −1, 7), **v**2 = (0, 4, −6) and the scalar

t = 3, we have

**v** + **v** = (−2 + 0, −1 + 4, 7 + (−6)) = (−2, 3, 1) = −2**i** + 3**j** + **k**,

1

2

t**v**1 = (3 · (−2), 3 · (−1), 3 · 7) = (−6, −3, 21) = −6**i** − 3**j** + 21**k**.





258

6 Vectors in a Three-Dimensional Space

**6.2 Scalar Product of Vectors**

Recall (see page [223](#br234)) that the scalar product of the two vectors **a** = (x , y , z )

a

a

a

and **b** = (x , y , z ) is denoted by **a** · **b** and determined through their coordinates as

b

b

b

follows:

**a** · **b** = x x + y y + z z .

(6.7)

a

b

a

b

a b

It is easy to verify that for scalar products of basis vectors the series of equalities

is valid:

**i** · **j** = **i** · **k** = **j** · **k** = 0 and **i** · **i** = **j** · **j** = **k** · **k** = 1.

(6.8)

**Theorem 6.1** The scalar product of the two vectors **a** and **b** is equal to the product

of the moduli of these vectors by the cosine of the angle α between them.

The concepts of projection of a vector on a line and scalar product of vectors are

closely connected. Indeed, since the projection of the vector **a** on the line, containing

the vector **b**, is equal to Pr **a** = |**a**| cos α and, on the other hand, Pr **b** = |**b**| cos α,

**b**

**a**

then we can write

**a** · **b** = |**a**||**b**| cos α = |**a**| Pr **b** = |**b**| Pr **a**.

(6.9)

**a**

**b**

If **a**·**b** = 0, but **a** = **0** and **b** = **0**, then such vectors are referred to as **orthogonal**,

since the angle between them is equal to π/2. Recall (see page [224](#br235)) that the notation

of the form **a** ⊥ **b** is used to denote orthogonality of vectors.

Example 6.2 Compute the scalar product of the vectors **a** = (3, 2, 1) and **b** =

(0, 2, 1).

**Solution**

**a** · **b** = 3 · 0 + 2 · 2 + 1 · 1 = 5.

(6.10)

The length |**a**| of the vector **a** = (x , y , z ) is computed by the formula:

a

a

a

\+

|**a**| = x2 + y2 + z2.

(6.11)

a

a

a

Example 6.3 Find the length of the vector **a** = (5, −3, −1).

**Solution** The length |**a**| is equal to 52 + (−3)2 + (−1)2 = 25 + 9 + 1 = 35.

\-

√

√





6.2 Scalar Product of Vectors

259

The **distance** between the points A(x , y , z ) and B(x , y , z ) is computed by

a

a

a

b

b

b

the formula:

\+

AB = (x − x )

2 +

(ya y )

−

2 +

(za z ) .

b

−

2

(6.12)

a

b

b

Example 6.4 Find the distance between the points A(5, 3, 2) and B(0, 3, 2).

**Solution**

\-

AB = (5 − 0)

2 + 3 − 3 2 + 2 − 2 2 = 5

(

)

(

)

.

(6.13)

Find the angle between two arbitrary vectors of a three-dimensional vector space.

Let the vectors **a** = (x , y , z ) and **b** = (x , y , z ) be given. Represent the

a

a

a

b

b

b

scalar product **a** · **b** in two ways, namely by the formulae ([6.7](#br269)) and ([6.9](#br269)):

**a** · **b** = x x + y y + z z ,

(6.14)

(6.15)

a

b

a

b

a b

**a** · **b** = |**a**||**b**| cos α.

Hence, we can conclude that the cosine of the angle α is equal to

x x + y y + z z

a

b

a

b

a b

cos α =

\+

.

(6.16)

(6.17)

\-

2 + 2 +

y

z

a

2

x

2 + 2 +

y

z

2

x

a

a

b

b

b

It is clear that

$

%

x x + y y + z z

a

b

a

b

a b

α = arccos

\+

.

\-

x

2 + 2 +

y

z

a

2

x

2 + 2 +

y

z

2

b

a

a

b

b

Example 6.5 Find the angle between the vectors **a** = (1, 2, 3) and **b** = (0, 2, 1).

**Solution** Using the formula ([6.17](#br270)), we obtain

$

%

1 · 0 + 2 · 2 + 3 · 1

7

α = arccos √

√

= arccos √

70

.

(6.18)

1 + 4 + 9 · 0 + 4 + 1

Example 6.6 Let two vectors be given: **a** = (5, 4, 1) and **b** = (2, −2, −2). Are

these vectors collinear or mutually orthogonal?





260

6 Vectors in a Three-Dimensional Space

**Solution** If the vectors are collinear, then there exists such a real number λ that the

condition **a** = λ**b** is satisﬁed. Hence, it follows:

xa

xb

ya

yb

za

zb

\=

\=

.

(6.19)

5

2

4

1

But since there exist two inequalities

non-collinear.

\=

\=

, then the vectors **a** and **b** are

−2

−2

In order to check the mutual orthogonality of the vectors, ﬁnd the scalar product

of **a** · **b**:

**a** · **b** = 5 · 2 − 4 · 2 − 1 · 2 = 0.

(6.20)

Then, the vectors **a** and **b** are mutually orthogonal.

**6.3 Vector Product of Vectors**

A **vector product**, or **cross product**, of two vectors speciﬁed in Cartesian coordi-

nate system as **a** = (x , y , z ) and **b** = (x , y , z ) is a vector denoted by **a** × **b**,

a

a

a

b

b

b

or [**a**, **b**], and determined according to the rule:




` `**i j k** 


**a** × **b** = x y z

` `=

(ya zb za yb)**i** (za xb xa zb)**j** (xa yb xb ya)**k**.

·

−

·

\+

·

−

·

\+

·

−

·


a

a

a




x y z

b

b

b

(6.21)

**6.3.1 Properties of the Vector Product**

For the arbitrary vectors of the three-dimensional vector space R3, the following

properties are valid.

**Property 1**

|**a** × **b**| = |**a**||**b**| sin α,

where α is the angle between **a** and **b**.

(6.22)

(6.23)

**Proof** Prove that the equality is valid:

2

2

2

2

|**a** × **b**| = |**a**| |**b**| sin α.





6.3 Vector Product of Vectors

261

Express |**a** × **b**|2 in terms of the coordinates of the initial vectors:

2

2

2

2

2

a

2

b

|**a** × **b**| = (y z − z y ) + (z x − x z ) + (x y − x y ) = y z

a

b

a

b

a

b

a

b

a

b

b

a

2

2

2

2

2

2

2

2

2 2

+z y + z x + x z + x y + x y − 2y z z y

a

b

a

b

a

b

a

b

b

a

a b a b

−2z x x z − 2x y x y .

a

b

a

b

a b b a

On the other hand, the right side of the equality ([6.23](#br271)) can be represented in the

form:

2

2

2

2

2

2

2

a

2

a

2

a

2

b

2

b

2

b

|**a**| |**b**| sin α = |**a**| |**b**| (1 − cos α) = (x + y + z )(x + y + z )

2

2

2

b

2

2

2

2

2

2

b

2

a

2

b

−(x x + y y + z z ) = x x + x y + x z + y x + y y

a

b

a

b

a

b

a

a

b

a

b

a

2

2

b

2

a

2

b

+y z + z x

a

2

2

b

2

a

2

b

2

a

2

b

2

a

2

b

2 2

b

+z y + z z − x x − y y − z z − 2x x y y

a

a

a b a b

−2x x z z − 2y y z z

a

b

a

b

a

b

a

b

2

2

2

2

2

2

2

2

b

2

a

2

b

2 2

= y z + z y + z x + x z + x y + x y − 2y z z y

a

b

a

b

a

b

a

b

a

a b a b

−2z x x z − 2x y x y .

(6.24)

a

b

a

b

a b b a

From the relation |**a** × **b**|2 = |**a**|2|**b**|2 sin2 α, we ﬁnally arrive at the conclusion

that |**a** × **b**| = |**a**||**b**| sin α.

Hence, it follows: if **a** and **b** are collinear, then **a** × **b** = 0 (since sin 0 = 0 and

sin π = 0).

**Property 2** If the vectors **a** and **b** are non-collinear, then the vector **c** = **a** × **b** is

orthogonal to each of the vectors **a** and **b**.

**Proof** Expand the scalar product of the vectors with regard to their coordinates:

(**a**×**b**)·**a** = y z x −z y x −x z y +z x y +x y z −y x z = 0. (6.25)

a

b

a

a

b

a

a

b

a

a

b

a

a

b

a

a b a

Similar to formula ([6.25](#br272)), we obtain that (**a** × **b**) · **b** = 0.

Therefore, the vector **c** is orthogonal to both the vector **a** and the vector **b**.

**Property 3**

**a** × **b** = −**b** × **a**.

(6.26)

**Property 4**

**a** × (**b** + **c**) = **a** × **b** + **a** × **c**,

(**a** + **b**) × **c** = **a** × **c** + **b** × **c**.

(6.27)

(6.28)





262

6

Vectors in a Three-Dimensional Space

**Fig. 6.3** To the computation

of the area of the triangle

ABC (Example [6.8](#br273))

B

D

A

C

Example 6.7 The vectors **a** = (3, −1, −2) and **b** = (1, 2, −1) are given. Find the

coordinates of the vector (2**a** − **b**) × (2**a** + **b**).

**Solution** Determine the coordinates of the new vectors: 2**a** − **b** = (5, −4, −3) and

2**a** + **b** = (7, 0, −5). Then, the sought-for vector will be equal to





**i j k** 



` `= 20 + 4 + 28

(6.29)

5 −4 −3

**i**

**j**

**k**.



7 0 −5

We obtain the answer: (20, 4, 28).

Example 6.8 The points A(1, 2, 0), B(3, 0, −3) and C(5, 2, 6) are given. Compute

the area S of the triangle ABC (see Fig. [6.3](#br273)).

ABC

The square of the triangle ABC is a half of the square of parallelogram, formed

−→

−→

by the vectors AB = (2, −2, −3) and AC = (4, 0, 6). Therefore,

1

2

1 −→ −→

SABC

\=

SABDC

\=

|AB × AC|.

(6.30)

(6.31)

2

Then,




**i j k** 

−→ −→


AB × AC = 2 −2 −3

` `= −12 − 24 + 8

**i**

**j**

**k**.




4 0 6 

Hence,

\-

1

2

SABC

\=

122 + 242 + 82 = 14

.

(6.32)





6.4 Scalar Triple Product

263

**6.4 Scalar Triple Product**

The **scalar triple product**, or **mixed product**, of the vectors **a**, **b** and **c** is the

number (**a**, **b**, **c**), resulting from computation of the expression (**a** × **b**) · **c**. First, the

vectors **a** and **b** are multiplied vectorially, and then, the resulting vector is multiplied

by **c** scalarly.

It is easy to verify the formula that expresses the scalar triple product in terms of

their coordinates:

(**a**, **b**, **c**) ≡ ((**a** × **b**) · **c**) = (y z − z y )x + (z x − x z )y + (x y − y x )z

a

b

a

b

c

a

b

a

b

c

a

b

a

b

c






x y z 

a

a

a


\= 

` `.

(6.33)

x y z 

b

b

b


x y z

c

c

c

For designation of the triple scalar product (**a** × **b**) · **c**, the notation (**abc**) is also

used.

**6.4.1 Properties of Scalar Triple Product**

**Property 1**

(**a** × **b**) · **c** = **a** · (**b** × **c**) = (**c** × **a**) · **b**.

**Property 2**

(6.34)

(6.35)

abs((**a** × **b**) · **c**) = Vn,

where Vn is the volume of the parallelepiped formed by the vectors **a**, **b** and **c** (see

Fig. [6.4](#br275)).

**Proof** By the deﬁnition of numeric projection of the vector **c** on the line, speciﬁed

by the vector **a** × **b**, the equality is valid:

(**a** × **b**) · **c** = |**a** × **b**| Pr**a**×**b c**,

(6.36)

where |**a** × **b**| = S the area of the parallelogram lying in the base of the

parallelepiped.

The vector **a** × **b** is orthogonal to the base of the parallelepiped, and, therefore,

Pr

**c** coincides with the height of the parallelepiped h.

**a**×**b**





264

6 Vectors in a Three-Dimensional Space

**Fig. 6.4** To the computation

of the volume of the

parallelepiped

D

C

B

A

**c**

C

D

**a**

B

**b**

A

Thus,

abs((**a** × **b**) · **c**) = S · h,

(6.37)

as we set out to prove.

Note Since the tetrahedron ABCA forms one-sixth part of the volume of the

parallelepiped, its volume is equal to

1

1

VABCA = Vn = abs((**a** × **b**) · **c**).

(6.38)

6

6

Three vectors are called **coplanar** if all of them are parallel to the same plane.

**Property 3** The vectors **a**, **b** and **c** are coplanar if and only if (**a**, **b**, **c**) = 0.

Example 6.9 Let the vertices of the tetrahedron be given A(2, −1, 1), B(5, 5, 4),

C(3, 2, −1) and D(4, 1, 3). Compute its volume.

−→

−→

−→

**Solution** Let us make the vectors AB = (3, 6, 3), AC = (1, 3, −2) and AD =

(2, 2, 2). Then, the volume of the tetrahedron ABCD is equal to

⎡

⎤

3 6 3

1

−→ −→ −→

1

⎢

⎥

VABCD = abs(AB × AC) · AD) = abs det 1 3 −2

⎢

⎥

(6.39)

⎣

⎦

6

6

2 2 2

⎡

⎤

1 2 1

1

6

⎢

⎥

\=

· 3 · 2 · abs det ⎢1 3 −2⎥ = abs(−3) = 3.

(6.40)

⎣

⎦

1 1 1





6.5 Vector Triple Product

265

Example 6.10 Find whether the following vectors are coplanar **a** = (2, −1, 2),

**b** = (1, 2, −3) and **c** = (3, −4, 7).

**Solution** Find the scalar triple product of the given vectors:





2 −1 2




(**a**, **b**, **c**) = 1 2 −3

` `= 2 · 14 − 12 + 1 · 7 + 9 + 2 · −4 − 6 = 0

(

)

(

)

(

)

.

(6.41)



3 −4 7 

Therefore, the vectors **a**, **b** and **c** are coplanar.

**6.5 Vector Triple Product**

Having three vectors, for example, **a**, **b** and **c**, apply the vector product operation

ﬁrst to **b** and **c**, and then vectorially multiply **a** and **b** × **c**. As a result, we obtain the

**vector triple product a** × (**b** × **c**).

**Theorem 6.2** For arbitrary vectors of a three-dimensional vector space **a**, **b** and **c**,

the identity is valid:

**a** × (**b** × **c**) ≡ **b**(**a** · **c**) − **c**(**a** · **b**).

For proof see Problem [**6.12**](#br278).

Note The relation ([6.42](#br276)) is also referred to as **Lagrange’s identity**.

**Consequence**. For the operation of vector triple product, the **Jacobi identity** is

(6.42)

valid:

**a** × (**b** × **c**) + **c** × (**a** × **b**) + **b** × (**c** × **a**) ≡ **0**.

(6.43)

**Proof** For each of the three summands of the sum, use the expansion ([6.42](#br276)):

**a** × (**b** × **c**) = **b**(**a** · **c**) − **c**(**a** · **b**),

**b** × (**c** × **a**) = **c**(**b** · **a**) − **a**(**b** · **c**),

**c** × (**a** × **b**) = **a**(**c** · **b**) − **b**(**c** · **a**).

(6.44)

(6.45)

(6.46)

Computation of the sum of the three vector products ([6.44](#br276))–([6.46](#br276)) after collect-

ing similar summands results in zero. The consequence is proved.





266

6 Vectors in a Three-Dimensional Space

**Review Questions**

\1. Deﬁne geometric vector.

\2. What are zero vector and unit vector?

\3. What vectors are called collinear?

\4. What is the condition of equality of vectors?

\5. Formulate the rule of parallelogram for addition of vectors.

\6. How is the projection of the vector **b** onto the vector **a** determined?

\7. What is the Cartesian coordinate system?

\8. Enumerate the normalizing vectors of the Cartesian coordinate system. How can

one use them to expand an arbitrary vector in the Cartesian basis?

\9. Deﬁne scalar product of vectors.

\10. What vectors are called orthogonal?

\11. How do we ﬁnd the distance between the two points speciﬁed by their Cartesian

coordinates?

\12. Deﬁne vector product of vectors.

\13. Enumerate the properties of a vector product.

\14. Deﬁne scalar triple product of vectors.

\15. Enumerate the properties of a scalar triple product.

\16. What three vectors are called coplanar?

\17. What is vector triple product?

\18. Write Lagrange’s identity for the vector triple product.

\19. Write the Jacobi identity.

**Problems**

**6.1.** Compute the scalar and vector products of the vectors **c**1 = 2**a** − **b** and

**c**2 = −**a** + 3**b**, if:

(a) **a** = (−2, 1, 1), **b** = (3, −2, 4);

(b) **a** = (2, 1, −2), **b** = (−1, 0, −2).

**6.2.** There are given vertices of the triangle ABC. Compute its area and the

cosine of the inner angle at the vertex B:

(a) A(2, 1, 0), B(3, 0, 3), C(2, −3, 7);

(b) A(4, −3, 2), B(−1, 4, 3), C(6, 3, −2).

**6.3.** Find whether vectors **a**, **b**, **c** are coplanar:

(a) **a** = (1, 1, 1), **b** = (2, 3, 0), **c** = (3, −1, −1);

(b) **a** = (−1, 0, −2), **b** = (0, 0, −1), **c** = (−1, 0, 3).

**6.4.** Prove that the points A(1, −1, 1), B(1, 3, 1), C(4, 3, 1) and D(4, −1, 1) are

vertices of a rectangle. Compute the length of its diagonals.





Problems

267

**6.5.** Compute the coordinates of the vector **c** that is orthogonal to the vectors

**a** = 2**j** − **k** and **b** = −**i** + 2**j** − 3**k** and forms an obtuse angle with the axis

√

Oy, if |**c**| = 7.

**6.6.** Find the angle between the vectors **a** + **b** and **a** − **b**, if **a** = 3**i** − **j** + 2**k** and

**b** = **i** + **j** − **k**.

**6.7.** The vectors **a** and **b** form the angle π/3. Find the length of the vector **a**−2**b**,

if |**a**| = 2, |**b**| = 1.

**6.8.** For what value of the real parameter d are the vectors **a** = (12, 2, d) and

**b** = (−3, 17d, −1) orthogonal?

**6.9.** For what value of the real parameter  will the vectors of the three-

dimensional Euclidean vector space **t**1 = **a** − 10**b** and **t**2 = **a** + **b** be

orthogonal, if |**a**| = 5, |**b**| = 3, and the angle ϕ between the vectors **a** and **b**

π

is equal to

?

6

**6.10.** For what value of the real parameter  will the vectors of the three-

dimensional Euclidean vector space **t**1 = 2**a** + **b** and **t**2 = **b** − 2**a** be

orthogonal, if |**a**| = 1, |**b**| = 3/2, and the angle ϕ between the vectors **a** and

2π

**b** is equal to

?

3

**6.11.** The vectors **a** and **b** have, in Cartesian basis, the coordinates **a** = (a , a , 0)

1

2

and **b** = (b , b , 0). Find the sine of the angle between these vectors.

1

2

**6.12.** Prove the theorem on vector triple product ([6.42](#br276)).

**6.13.** Prove the identities valid for the arbitrary vectors **a**, **b**, **c** and **d**:

(1) (**a** × **b**) · (**c** × **d**) ≡ (**a** · **c**)(**b** · **d**) − (**a** · **d**)(**b** · **c**);

(2) (**a** × **b**) × (**c** × **d**) ≡ **c**(**abd**) − **d**(**abc**);

(3) **a** × (**b** × (**c** × **d**)) ≡ (**b** · **d**)(**a** × **c**) − (**b** · **c**)(**a** × **d**);

(4) (((**a** × **b**) × (**b** × **c**))((**b** × **c**) × (**c** × **a**))((**c** × **a**) × (**a** × **b**))) ≡ (**abc**)4.

**6.14.** Prove the identity valid for the arbitrary vectors **a**, **b**, **c**, **d**, **e**, **f** :

(**a** × **b**) · ((**c** × **d**) × (**e** × **f** )) ≡ (**abd**)(**cef** ) − (**abc**)(**def** ).

∗**6.15.** Simplify the vector expression that depends on the natural parameter n:

**f**

= (**a** × · · · × (**a** × (**a** × **b**)) . . . ) .

n



!

n products

**6.16.** Prove that for **p** , **p** , **p** , **p** , **p** ∈ R3 the equality is fulﬁlled:

1

2

3

4

5






(**p**1**p**2**p**4) (**p**1**p**2**p**5)

(**p**1**p**2**p**3)(**p**1**p**4**p**5) =


.


(**p p p** ) (**p p p** )

1

3

4

1 3 5





268

6 Vectors in a Three-Dimensional Space

∗**6.17.** Solve the system of linear equations, represented in vector form, relative to

the unknown variables x , x , x :

1

2

3

**α** · **x** = γ,

**α** × **x** + **β** = **0**,

where **x** = (x , x , x ), and the vectors **α** = **0**, **β** and the scalar γ do not

1

2

3

depend on x , x , x .

1

2

3

∗**6.18.** Solve the system of linear equations, represented in vector form, relative to

the unknown variables x , x , x :

1

2

3

**α** · **x** = c1,

**β** · **x** = c2,

**γ** · **x** = c3,

where **x** = (x , x , x ), and the vectors **α**, **β**, **γ** and the constants c , c , c

1

2

3

1

2

3

do not depend on x , x , x and (**α**, **β**, **γ** ) = 0.

1

2

3

∗**6.19.** Solve the system of equations relative to the unknown vectors **x** and **y**:

**π** × **x** + **ρ** × **y** = **σ**,

**ρ** × **x** − **π** × **y** = **τ**,

where **π**, **ρ**, **σ**, **τ** ∈ Rn, and the vectors **π** and **ρ** are not equal to the zero

vector simultaneously.

**Answers and Solutions**

[**6.1**](#br277)[** ](#br277)Solution.

(a) Write the vectors **c** and **c** in coordinate form:

1

2

**c** = 2(−2, 1, 1) − (3, −2, 4) = (−7, 4, −2), **c** = −(−2, 1, 1)

1

2

+3(3, −2, 4) = (11, −7, 11).

The scalar product is equal to **c** · **c** = −7 · 11 + 4 · (−7) − 2 · 11 = −127.

1

2





Answers and Solutions

269

The vector product is equal to





` `**i**

**j**

**k** 


**c** × **c** = −7 4 −2

` `= 30 + 55 + 5 = 30 55 5

**i**

**j**

**k**

(

,

, ).

1

2



11 −7 11

(b) Write the vectors **c** and **c** : c = (5, 2, −2), c = (−5, −1, −4).

1

2

1

2

Their scalar product is equal to **c** ·**c** = 5·(−5)+2·(−1)−2·(−4) = −19.

1

2

The vector product:





` `**i**

**j**

**k** 


**c** × **c** =

5

2 −2

` `= −10 + 30 + 5 = −10 30 5

**i**

**j**

**k**

(

,

, ).

1

2



−5 −1 −4

[**6.2**](#br277)[** ](#br277)Solution.

−→

−→

(a) Compute the coordinates of the vectors BA and BC:

−→

BA = (2 − 3, 1 − 0, 0 − 3) = (−1, 1, −3),

−→

BC = (2 − 3, −3 − 0, 7 − 3) = (−1, −3, 4).

Then, ﬁnd the cosine of the angle ϕ at the vertex B:

−→ −→

BA · BC

−1 · (−1) + 1 · (−3) + (−3) · 4

cos ϕ =

= -

\-

−→ −→

(−1)

2 + 12 + −3 2 ·

(

)

(

−1 2 + −3 2 + 42

)

(

)

|BA| · |BC|

14

= −√

.

286

The area can be computed in two ways.

T h e f i r s t m e t h o d

−→

−→

The product of the vectors BA and BC is determined as





` `**i**

**j**

**k** 

−→ −→


BA×BC = −1 1 −3

` `= 4−9 − −4−3 + 3+1 = −5 +7 +4

(

)**i**

(

)**j**

(

)**k**

**i**

**j**

**k**.



−1 −3 4 

Substitute the obtained values of the coordinates into the formula for the area

of the triangle:

1-

3

2

√

10

1 −→ −→

S = |BA × BC| =

(−5)2 + 72 + 42 =

.

2

2





270

6 Vectors in a Three-Dimensional Space

T h e s e c o n d m e t h o d

According to the fundamental trigonometric identity (see Appendix [B](#br417),

formula ([B.1](#br417))), we have

.

1 −

√

+1 − cos2 ϕ =

.

142

286

3 10

= √

286

sin ϕ =

Substitute the coordinate values into the area formula:

1 −→ −→

S = |BA| · |BC| · sin ϕ

2

√

1-

\-

3 10

3

2

√

\10.

\=

(−1)2 + 12 + (−3)2 · (−1)2 + (−3)2 + 42 · √

\=

286

2

Obviously, both methods of computing the area of the triangle result in the

same answer:

√

14

cos ϕ = −√

286

3

2

, S =

\10.

−→

−→

(b) The coordinates of the vectors BA and BC are equal to

−→ −→

BA = (5, −7, −1), BC = (7, −1, −5).

Compute the cosine of the angle ϕ between these vectors:

−→ −→

(BA · BC)

5 · 7 + (−7) · (−1) + (−5) · (−1)

47

75

cos ϕ=

= -

\-

\=

)

.

−→ −→

5

2 + −7 2 + −1 2 · 72 + −1 2 + −5 2

(

)

(

)

(

)

(

|BA| · |BC|

−→

−→

Then, compute the vector product of BA and BC:





**i j k** 

−→ −→


BA × BC = 5 −7 −1

` `= 34 + 18 + 44

**i**

**j**

**k**.



6 −1 −5

Substitute the coordinate values into the area formula:

\-

√

854

.

1 −→ −→

S = |BA × BC| =

1

2

·

342 + 182 + 442 =

2





Answers and Solutions

271

We ﬁnally obtain

√

47

75

cos ϕ =

,

S = 854.

[**6.3**](#br277)[** ](#br277)Solution.

(a) Since the determinant composed of the vector coordinates is not equal to zero:





1 1

2 3

1

0





` `= −12

,



3 −1 −1

then the vectors **a**, **b** and **c** are not coplanar.

(b) The determinant composed of the vector coordinates is equal to zero:





−1 0 −2





` `= 0

0 0 1

,



−1 0 3 

and, therefore, these vectors are coplanar.

[**6.4**](#br277)[** ](#br277)Solution.

Note that the points A, B, C and D lie in the same plane, since the applicate of

all these points is equal to z = 1.

Let us prove that these four points are vertices of a parallelogram. We have to

prove that

−→

−→

−→

−→

|AB| = |CD|, |BC| = |AD|.

Find the coordinates of the vectors introduced for consideration:

−→

AB = (1 − 1, 3 − (−1), 1 − 1) = (0, 4, 0),

−→

CD = (4 − 4, −1 − 3, 1 − 1) = (0, −4, 0),

−→

BC = (4 − 1, 3 − 3, 1 − 1) = (3, 0, 0),

−→

AD = (4 − 1, −1 − (−1), 1 − 1) = (3, 0, 0).





272

6 Vectors in a Three-Dimensional Space

Therefore,

⎧

√

−→

⎪ | | = 02 + 42 + 02 = 4

⎪ AB

,

⎪

⎪

√

⎪ −→

−→

−→

−→

⎨

|CD| = 02 + 42 + 02 = 4,

|AB| = |CD|,

√

√

⇒

−→

−→

|BC| = |AD|.

⎪

2

2

2

⎪ |BC| = 3 + 0 + 0 = 3,

⎪

⎪

⎪ −→

⎩

|AD| = 32 + 02 + 02 = 3;

π

If one of the parallelogram angles is equal to , then all other angles are also equal

2

π

to

.

2

−→

−→

Show that the scalar product of the vectors AB and AD is equal to zero:

−→ −→ −→ −→

AB · AD = 0 · 3 + 4 · 0 + 0 · 0 = 0 ⇒ AB ⊥ AD.

Therefore, ABCD is a rectangle. Find its diagonals with the help of the Pythagorean

theorem:

\-

\-

AC = AB2 + BC2 = 42 + 32 = 5.

It is clear that AC = BD, since the diagonals of the rectangle are equal.

As a result, we obtain AC = BD = 5.

[**6.5**](#br277)[** ](#br277)Solution.

Let **c** = (c , c , c ), where c , c , c are the unknown coordinates of the vector.

x

y

z

x

y

z

The condition of orthogonality of **a** and **c** has the form **a** · **c** = 0, or 2c − c = 0.

y

z

Then, the condition of orthogonality of **b** and **c** is **b** ·**c** = 0, or −c +2c −3c = 0.

√

x

y

z

Since |**c**| = 7 and the length of the vector is equal to the square root of the

\+

√

sum of squares of its coordinates, c2 + c2 + c2 = 7, which can be written as

x

y

z

c

2 + 2 + 2 = 7.

c

c

x

y

z

We obtain the system of three equations relative to the variables c , c , c :

x

y

z

⎧

⎪

2

−

= 0

⎪

cy cz

,

⎨

−c + 2c − 3c = 0,

⎪

x

y

z

⎪

⎩

c

2 + 2 + 2 = 7

c

c

.

x

y

z

As the independent variable select c and express through it two other variables

y

of the system: c = 2c and c = 2c − 3c = 2c − 3(2c ) = −4c . Therefore,

z

y

x

y

z

y

y

y

**c** = (−4c , c , 2c ) = c (−4, 1, 2), where c ∈ R.

y

y

y

y

y





Answers and Solutions

273

√

The length of the vector **c** is equal to |**c**| = 7, and, therefore,

√

\-

√

7

1

1

abs(c ) (−4)2 + 12 + 22 = 7, abs(cy) = √ = √ , and c = ± √ .

y

y

21

3

3

According to the problem statement, the vector **c** forms an obtuse angle with the

axis Oy, i.e. cosϕ < 0, where ϕ is the angle between the vectors **c** and **j**. Since

**c** · **j**

c

y

cos ϕ =

= √ < 0,

7

|**c**||**j**|

1

c = −√ .

y

3

1

We ﬁnally obtain **c** = √ (4, −1, −2).

3

[**6.6**](#br278)[** ](#br278)Solution.

Write the vectors **a** and **b** in coordinate form:

**a** = (3, −1, 2),

**b** = (1, 1, −1).

Then, the sum and the difference of these vectors are

**a** + **b** = (3 + 1, −1 + 1, 2 + (−1)) = (4, 0, 1),

**a** − **b** = (3 − 1, −1 − 1, 2 − (−1)) = (2, −2, 3).

Use the formula of the cosine of the angle α between the vectors:

(**a** · **b**)

cos α =

.

|**a**| · |**b**|

After simple computations, we obtain

(**a** + **b**) · (**a** − **b**)

|**a** + **b**| · |**a** − **b**|

4 · 2 + 0 · (−2) + 1 · 3

11

17

cos α =

= √

\-

\=

2

.

4 + 0 + 1 · 2 + (−2) + 3

2

2

2

2

2

11

Therefore, α = arccos

.

17





274

6 Vectors in a Three-Dimensional Space

[**6.7**](#br278)[** ](#br278)Solution.

Compute |**a** − 2**b**|2:

2

2

2

|**a**−2**b**| = (**a**−2**b**)·(**a** −2**b**) = **a**·**a**−4**a**·**b**+4**b**·**b** = |**a**| −4|**a**||**b**| cos ϕ +4|**b**| ,

where ϕ = π/3 is the angle between the vectors **a** and **b**. Having substituted numeric

values, we obtain |**a** − 2**b**|2 = 1, and, therefore, |**a** − 2**b**| = 1.

[**6.8**](#br278)[** ](#br278)Solution.

As is known, the necessary and sufﬁcient condition of orthogonality of two

vectors is that their scalar product is equal to zero: **a**·**b** = 0. Substitute the coordinate

values from the problem statement:

12 · (−3) + 2 · 17d − 1 · d = 0,

12

d =

.

11

12

11

Therefore, the vectors **a** and **b** are orthogonal for the parameter value d =

[**6.9**](#br278)[** ](#br278)Solution.

.

In order for the vectors to be orthogonal, their scalar product must be equal to

zero: **t** · **t** = 0,

1

2

(**a** − 10**b**) · (**a** + **b**) = 0,

**a** · **a** + **a** · **b** − 10**a** · **b** − 10**b** · **b** = 0.

√

10 3 − 10

Then, we ﬁnd  =

[**6.10**](#br278)[** ](#br278)Solution.

√

.

3 3 − 36

The necessary condition of the vector orthogonality: **t** · **t** = 0, or

1

2

(2**a** + **b**) · (**b** − 2**a**) = 0,

2

2

2**ab** − 4|**a**| + |**b**| − 2**ab** = 0.

3

9 3

Substitute the numeric values from the problem statement: − −4+

\+

\=

2

2

4

22

15

0, and, therefore,  =

.

a1b2 − a2b1

[**6.11**](#br278)[** ](#br278)Answer: sin ϕ = +

\+

.

2

2

2

2

2

a + b a + b

1

1

2





Answers and Solutions

275

[**6.15**](#br278)[** ](#br278)Answer:

a(**a** × **b**),

if n is odd,

**f**

= (−1)n/2 an−2

n

a **b** (**a b**)**a**,

−

2

·

if is even

n .

[**6.17**](#br278)[** ](#br278)Answer:

γ

1

a2

**x** =

**α** + **α** × **β**.

α2

[**6.18**](#br279)[** ](#br279)Answer:

$

%

1

**x** =

c (**β** × **γ** ) + c (**γ** × **α**) + c (**α** × **β**) .

1

2

3

(**α**, **β**, **γ** )

[**6.19**](#br279)[** ](#br279)Solution.

Multiply the ﬁrst equation of the system by the vector **ρ** scalarly on the right;

multiply the second equation by the vector **π** scalarly on the right. Subtracting one

equation from the other, we ﬁnd

**π** × **σ** + **ρ** × **τ**

**x** = −

\+ γ **π** + γ **ρ**,

1

2

2 +

**ρ**

2

**π**

where γ , γ are real numbers.

1

2

Having substituted the obtained expression into the ﬁrst equation of the system,

we ﬁnd **y**:

**π** × **τ** − **ρ** × **σ**

**y** =

\+ γ **π** − γ **ρ**.

2

1

2 +

**ρ**

2

**π**





**Chapter 7**

**Equation of a Straight Line on a Plane**

**7.1 Slope-Intercept Form of the Equation of a Straight Line**

Consider Cartesian coordinate system on a plane.

Let the straight line L intersect the axis Oy at the point B with the coordinates

(0, b) and forms with the axis Ox the angle α (see Fig. [7.1](#br288)). For deﬁniteness, we

π

will assume that the angle α <

.

2

On the line, take an arbitrary point A with the coordinates (x, y). Then, from the

point A, drop a perpendicular to the axis Ox, and from the point B, a perpendicular

to the axis Oy. Consider the obtained triangle ABC. It is obvious that BC = x,

AC = y − b, ABC = α. Since AC = BC tan α, we obtain y − b = x · tan α or

y = tan α · x + b.

Denote the tangent of the angle α by k. The variable k = tan α is referred to as

the **slope** of the straight line on the plane. As a result, we arrive at the equation of a

straight line of the form:

y = kx + b.

(7.1)

It is called the **slope-intercept form of the equation of a straight line**.

Note For the lines of the form y = const, the slope is equal to zero; for the lines of

the form x = const, the slope is undeﬁned.

© Springer Nature Switzerland AG 2021

277

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_7>





278

7

Equation of a Straight Line on a Plane

**Fig. 7.1** The line L on the

plane xOy

y

A(x, y) L

B(0, b)

C

α

x

O

**Fig. 7.2** Construction of

**n**—a normal vector to the line

y

**n**

x

O

**7.2 General Equation of a Straight Line**

**General equation of a straight line on a plane** has the form:

Ax + By + C = 0.

(7.2)

The real numbers A, B and C are called **coefﬁcients of the straight line**

**equation**.

The variables A and B cannot simultaneously be equal to zero, because, in this

case, if C = 0, then all points on the plane will satisfy this equation. However, if

C = 0, then none of the points on the plain satisﬁes this equation.

⎡ ⎤

A

The vector **n** = ⎣ ⎦ is called a **normal vector** of a line or a **normal**. The

B

normal vector is orthogonal to the respective line (see Fig. [7.2](#br288)).

Let the inequality B = 0 be valid. In this case, the summand By can be

rearranged to the right, and both parts of the equation can be divided by −B = 0.





7.3 Slope-Intercept Form of the Equation of a Straight Line Through a Given. . .

279

(7.3)

(7.4)

As a result, we obtain

Ax + C = −By

or

A

B

C

−

x − = y.

B

A

C

Let us introduce notations − = k and − = b; then, we arrive at the equation

B

B

y = kx [+](#br287)[ ](#br287)b, which is a slope-intercept form of the equation of a straight line

(see Eq. ([7.1](#br287))).

**7.3 Slope-Intercept Form of the Equation of a Straight Line**

**Through a Given Point**

Consider the slope-intercept form of the equation of a straight line:

y = kx + b.

(7.5)

Let this straight line pass through a point with the coordinates (x , y ). Substitute

0

0

these coordinates into the equation:

y0 = kx0 + b.

(7.6)

Subtract from the Eq. ([7.5](#br289)) the Eq. ([7.6](#br289)). We obtain the sought **slope-intercept form**

**of the equation of a straight line passing through the given point**:

(y − y0) = k(x − x0).

(7.7)

Example 7.1 Find the slope-intercept form of the equation of a straight line k = 2

through T (1, 5).

**Solution** Use the formula ([7.7](#br289)). Then, we have

(y − 5) = 2(x − 1),

(7.8)

or

y = 2x + 3.

(7.9)





280

7 Equation of a Straight Line on a Plane

**7.4 Equation of a Straight Line Through Two Given Points**

Find the equation of a straight line through two given points T (x , y ) and

1

1

1

T2(x2, y2) subject to the condition that x1 [=](#br289)[ ](#br289)x2 and y1 = y2. For this purpose, write

the equation of a straight line in the form ([7.7](#br289)), assuming that is passes through the

point T1:

y − y1 = k(x − x1).

(7.10)

Since this line also passes through the point T2, then we will substitute its

coordinates into the Eq. ([7.10](#br290)):

y2 − y1 = k(x2 − x1).

Divide the Eq. ([7.10](#br290)) by Eq. ([7.11](#br290)). We obtain

(7.11)

(7.12)

y − y1

x − x1

.

\=

y2 − y1

x2 − x1

This is the **equation of a straight line through two given points**.

Note The formula ([7.12](#br290)) is not applicable in the case of equality of the abscissas or

equality of the ordinates of the initial points T and T . If x = x , then the equation

1

2

1

2

of the line T T has the form x = x . If the condition y = y is fulﬁlled, then the

1

2

1

1

2

equation of this line has the form y = y .

1

Example 7.2 Find the equation of the line through T (a, b) and T (b, a), where

1

2

a, b ∈ R, and a = b.

**Solution** Use the formula ([7.12](#br290)). Substitute into it the coordinates of the points

x1 = a, y1 = b, x2 = b, y2 = a:

y − b

x − a

\=

.

(7.13)

a − b

b − a

After simple transformations, we obtain the equation of the straight line:

y − b = −(x − a),

x + y − a − b = 0.

(7.14)

(7.15)





7.5 Angle Between Two Straight Lines

281

**7.5 Angle Between Two Straight Lines**

Consider two straight lines speciﬁed by the equations y = k x+b and y = k x+b

1

1

2

2

(see Fig. [7.3](#br291)).

By the angle α between the lines, we will understand the angle by which one of

these lines should be turned around their intersection point, anticlockwise, until the

ﬁrst superposition on the other line.

From Fig. [7.3](#br291), it is seen that the angle α between the lines is equal to α − α .

1

2

And the equalities tan α1 = k and tan α = k are fulﬁlled. In this case, based

1

2

2

on the formula of tangent of a difference of two arguments (see formula ([B.14](#br418)) in

Appendix [B](#br417)), we can write

tan α − tan α

k − k

.

1

2

1

2

tan α = tan(α − α ) =

\=

(7.16)

1

2

1 + tan α · tan α

1 + k k

1

2

1 2

Hence,

k1 − k2

1 + k k

α = arctan

.

(7.17)

1

2

Having exchanged places of the parameters k and k , we obtain the tangent of

1

2

the **adjacent** angle 1ϕ = π − ϕ.

From the obtained formula ([7.17](#br291)) follow two consequences:

(a) The straight lines with the slopes k and k are orthogonal if the condition 1 +

1

2

1

k1k2 = 0 is fulﬁlled, which is equivalent to k2 = −

.

k1

(b) The straight lines are parallel if k = k .

1

2

Consider the straight lines speciﬁed by the equations in general form:

A1x + B1y + C1 = 0 and A2x + B2y + C2 = 0.

(7.18)

**Fig. 7.3** Deﬁnition of the

angle α between two straight

y

lines

α

α2

α1

x

O





282

7 Equation of a Straight Line on a Plane

A1

A2

Then, k1 = −B1 and k2 = −B2 . Therefore,

A2B1 − A1B2

A1A2 + B1B2

tan α =

.

(7.19)

From ([7.19](#br292)) directly follows that the lines speciﬁed by the Eqs. ([7.18](#br291)) are

orthogonal at A A + B B = 0 and parallel at A B − A B = 0.

1

2

1

2

2

1

1 2

Example 7.3 A straight line 2x − 5y + 1 = 0 is given. Set up the equation of a

straight line that passes through the point T (3, 3):

0

(a) parallel to this line;

(b) perpendicular to this line.

**Solution**

A

2

2

(a) Find the slope k0 = − = −

\=

5

.

B

(−5)

Write the equation of the straight line that passes through the given point

with the speciﬁed slope k = k :

1

0

y − y0 = k1(x − x0),

(7.20)

(7.21)

2

y − 3 = (x − 3).

5

Thus, the sought straight line has the form: 2x − 5y + 9 = 0.

(b) Find the slope of the line that is perpendicular to the given one: k = −

1

\=

2

k0

5

− .

2

Write the equation of the straight line that passes through the given point

with the speciﬁed slope k2:

y − y0 = k2(x − x0),

(7.22)

5

y − 3 = − (x − 3).

(7.23)

2

We obtain the equation of the straight line: 5x + 2y − 21 = 0.

**7.6 Intercept Form of the Equation of a Straight Line**

Consider the equation of the line Ax + By + C = 0, where the variables A, B and

C are not equal to zero.





7.7 Normal (Symmetric) Form of the Equation of a Line

283

**Fig. 7.4** The line that passes

through the points (a, 0) and

(0, b)

y

b

a

x

O

Let us transform it as follows:

A

C

B

−

x − y = 1.

(7.24)

(7.25)

C

C

C

B

Let us introduce notations: a = − and b = −

.

A

As a result, we obtain the equation:

x

y

b

\+

= 1,

a

which is the **intercept form of the equation of a straight line**.

It is obvious that the given line passes through the points with the coordinates

(a, 0) and (0, b). It is shown in Fig. [7.4](#br293).

Thus, this line cuts off segments of length abs(a) and abs(b) on the coordinate

axes.

**7.7 Normal (Symmetric) Form of the Equation of a Line**

Consider an arbitrary straight line L. Let us draw, through the origin of coordinates

O, a line, perpendicular to L, and denote by the letter P the intersection point of

these lines.

On the line OP, take the unit vector **n**, whose direction coincides with the

−→

direction of the vector OP.

−→

Assume that p = |OP|, and the angle θ is the angle between the vector **n** and

the axis Ox (see Fig. [7.5](#br294)).

Since **n** is a unit vector, its coordinates are equal to the projections of this vector

on the coordinate axes:

**n** = (cos θ, sin θ).

(7.26)





284

7

Equation of a Straight Line on a Plane

**Fig. 7.5** To the derivation of

the normal form of the

equation of a line

y

P

**n**

T x, y

(

)

θ

x

O

L

The arbitrary point T (x, y) lies on the considered line L if and only if the

−→

projection of the vector OT on the axis determined by the vector **n** is equal to

p:

−→

Pr OT = p.

(7.27)

**n**

As is well known,

−→

|**n**|

−→

·

−→

= OT · **n**.

OT

**n**

Pr OT =

(7.28)

**n**

−→

Bearing in mind that OT = (x, y), and the vector **n** is determined by the

equality ([7.26](#br293)), we obtain the following expression for their scalar product:

−→

OT · **n** = x cos θ + y sin θ.

(7.29)

From the above reasoning, it follows that the point T (x, y) lies on the line L if

and only if the coordinates of this point satisfy the relation:

x cos θ + y sin θ − p = 0.

(7.30)

Th[is](#br294)[ ](#br294)equation is called the **normal form of the equation of the line** L or the

**He[sse**](#br294)[**1](#br294)[ ](#br294)normal form**.

Let the straight line L be speciﬁed by the general equation:

Ax + By + C = 0,

(7.31)

where C = 0.

1 Ludwig Otto Hesse (1811–1874), German mathematician.





7.7 Normal (Symmetric) Form of the Equation of a Line

285

In order to transform the general equation of a line into a normal form, multiply

both sides of the equation by the so-called **normalizing factor**:

1

μ = −√

sgn(C),

(7.32)

A2 + B2

where sgn(C) is the sign of the coefﬁcient C determined by the rule:

⎧

⎪

⎪+1, if C > 0,

⎨

sgn(C) =

0 if = 0

(7.33)

,

C

,

⎪

⎪

⎩

−1, if C < 0.

As a result, the new coefﬁcients at x and y (namely, μA and μB) will satisfy the

condition:

2

2

(μA) + (μB) = 1.

(7.34)

If we select the angle θ so that cos θ = μA and sin θ = μB, while p =

−abs(μC), then we will obtain the normal form of the equation of a line.

Note If the condition C = 0 is fulﬁlled, then the line passes through the origin of

coordinates, and the normalizing factor can be taken with an arbitrary sign: μ =

1

± √

.

A

2 +

B2

Let us introduce the concept of **deviation** of an arbitrary point T (x, y) from the

given line L. Let the number d denote the distance from the point T to this line.

We will call the number + d the deviation δ of the point T from the line L in

the event when the point T and the origin of coordinates O lie on the opposite sides

of the line L and the number − d in the event when the points T and O lie on the

same side of L.

Show that the left side of the normal form of the equation of the line is equal to

the deviation of the point T (x, y) from this line.

Let Q be the projection of the point T on the axis determined by the vector **n**.

The deviation δ of the point T from the line L is equal to PQ.

From Fig. [7.6](#br296), it is seen that

δ = PQ = OQ − OP = OQ − p.

(7.35)

−→

But OQ = Pr OT = x cos θ + y sin θ. So,

**n**

OQ = x cos θ + y sin θ.

(7.36)





286

7 Equation of a Straight Line on a Plane

**Fig. 7.6** The deviation

δ = P Q of the point T from

the line L

y

L

Q

P

T(x, y)

**n**

x

O

Correlating the obtained formulae ([7.35](#br295)) and ([7.36](#br295)), we obtain

δ = x cos θ + y sin θ − p.

(7.37)

This brings us to the following rule: in order to ﬁnd the deviation δ of the point

T (x0, y0) from the line L, we should substitute to the left side of the normal form

of the equation of the line the coordinates x and y of the point T instead of x and

0

0

y. The distance from the point T to the line L is equal to the absolute deviation.

Example 7.4 Let us compute the distance from the point T (5, 4) to the line through

A(1, −2) and B(0, 3).

**Solution** Write the equation of a straight line through the points A and B:

x − 1

−1

y + 2

\=

or 5x + y − 3 = 0.

(7.38)

5

1

Having multiplied the resulting equality by μ = √ , we bring the equation to

26

the normal form:

5x

y

3

√

\+ √ − √ = 0.

26 26

(7.39)

26

Then, the distance d from the point T to the line is equal to


√

5 · 5

4

3

26

= √

d = abs

√

\+ √ − √

26 26

\=

26

\26.

(7.40)

26





7.8 Line Segments

287

**7.8 Line Segments**

**Line segment** M M is a part of a straight line between its two points M (x , y )

1

2

1

1

1

and M (x [,](#br420)[ ](#br420)[y](#br420)[ ](#br420)). The points M (x , y ) and M (x , y ) are the **endpoints** of the

2

[2](#br420)

2

1

1

1

2

2

2

segment [[8](#br420)[\].](#br420)

A set of points belonging to the segment is speciﬁed as follows:

M1M2 = {(x, y): x = (1 − t)x1 + tx2, y = (1 − t)y1 + ty2, t ∈ [0, 1]}.

There exists an equivalent notation of M M :

(7.41)

1

2

M1M2 = {(x, y): x = x1 +(x2 −x1)t, y = y1 +(y2 −y1)t, t ∈ [0, 1]}.

(7.42)

The variable 0  t  1 in the formulas ([7.41](#br297)) and ([7.42](#br297)) is referred to as the

**parameter** of the segment.

Example 7.5 Let us write a program in Python that determines, by the segment

endpoint coordinates, in which coordinate quadrants it is located. For example, the

segment L L that connects the points L (−1, −2) and L (4, 1), lies in the I, III and

1

2

1

2

IV quadrants. Another example: the segment that connects the points M (−1, −2)

1

and M (−1, −2) entirely belongs to the II quadrant (see Fig. [7.7](#br297), which shows the

2

segments L L and M M with the numbers of each quadrant).

1

2

1

2

**Solution** In order to represent a Cartesian plane point in the computer memory,

introduce a class Point, which contains two ﬁelds: x and y, the abscissa and

y

II

I

M1

M2

L2

x

O

L1

III

IV

**Fig. 7.7** To the Example [7.5](#br297). The segment L1L2 lies in the I, III and IV quadrants, while the

segment M M entirely belongs to the II quadrant

1

2





288

7 Equation of a Straight Line on a Plane

the ordinate of the point. Thus, the segment is determined by the boundary points;

denote them by P and P .

1

2

The main computing work is performedby the function get\_quadrants(p1,

p2). It returns the list that contains the numbers of the quadrants where the segment

P1P2 is located.

The auxiliary function get\_quadrant(p) is used to determine the number

of the quadrant to which the only argument belongs, namely the point p. This

function returns an integer number from the set {0, 1, 2, 3, 4}. The variable

get\_quadrant(p) is equal to zero if and only if p lies on the Ox or Oy axis

and therefore does not belong to any of the plane quadrants.

Execution of the function get\_quadrant(p1, p2) begins with checking

whether the points p1 and p2 lie in the adjacent quadrants, i.e. those that form the

unordered pairs 1–2, 2–3, 3–4, 4–1. During this check, the variables p1\_quad and

p2\_quad will be assigned the numbers of the quarters to which points p1 and p1

belong, respectively.

Since the numbers of the adjacent quadrants differ by one modulo two, the

False value of the boolean variable

is\_adjacent = abs(p1\_quad - p2\_quad) % 2 == 1

is a sufﬁcient condition of adjacency.

Then, the following operations are executed. If the points p1 and p2 lie in the

adjacent quadrants, then into the ﬁnal list are written the values p1\_quad and

p2\_quad, following which the function get\_quadrants() terminates.

Otherwise, the equality of the numbers p1\_quad and p2\_quad is checked. If

it is valid, then the entire segment lies in the quadrant number p1\_quad, and the

function get\_quadrants() terminates.

The last case of the opposite quadrants remains, i.e. of the pairs 1–3 or 2–4. The

line drawn through the points p1 and p2 intersects the ordinate axis at the point

with the coordinates (0, b), where

b = (p1.y p2.x - p1.x p2.y)/(p2.x - p1.x).

(7.43)

\*

\*

If p1\_quad = 1 or p1\_quad = 3, then at b > 0 it is necessary to additionally

write the second quadrant to ﬁnal list, and the fourth quadrant at b < 0. Otherwise

(in the case p1\_quad ∈ {2, 4}) at b > 0, it is necessary to additionally write the

ﬁrst quadrant to the list, and the third quadrant at b < 0.

Thus, all the possible cases of location of the segment P P relative to the

1

2

coordinate axes are exhausted, on the condition that none of the segment endpoints

lies on the coordinate axis.

Listing 7.1 provides the text of the program that determines, by the segment

endpoint coordinates, in which quadrants it is located.





7.8 Line Segments

289

§

Listing 7.1¤

1 class Point:

2

3

4

5

6

def \_\_init\_\_(self, x, y):

self.x = x

self.y = y

7 def get\_quadrant(p):

8

9

if p.x > 0 and p.y > 0:

return 1

10

11

12

13

14

15

16

17

18

19

elif p.x < 0 and p.y > 0:

return 2

elif p.x < 0 and p.y < 0:

return 3

elif p.x > 0 and p.y < 0:

return 4

else:

return 0

20 def get\_quadrants(p1, p2):

21

22

23

24

25

26

27

28

29

30

31

32

33

34

35

36

37

38

39

40

41

p1\_quad = get\_quadrant(p1)

p2\_quad = get\_quadrant(p2)

is\_adjacent = abs(p1\_quad - p2\_quad) % 2 == 1

if is\_adjacent:

return [p1\_quad, p2\_quad]

elif p1\_quad == p2\_quad:

return [p1\_quad]

else:

b = (p1.y \* p2.x - p1.x \* p2.y) \

/ (p2.x - p1.x)

if b == 0:

return [p1\_quad, p2\_quad]

elif p1\_quad == 1 or p2\_quad == 3:

quadrant = 2 if b > 0 else 4

return [p1\_quad, p2\_quad, quadrant]

else:

quadrant = 1 if b > 0 else 3

return [p1\_quad, p2\_quad, quadrant]

¦

¥





290

7 Equation of a Straight Line on a Plane

The most general case is when P or P can belong to the coordinate axes and

1

2

is discussed in Problem [**7.30**](#br302). The solution of this problem includes the function

get\_quadrants\_general(), which is free from the mentioned constraint.

**Review Questions**

\1. How is the slope of a straight line on a plane determined?

\2. Write the equation of a straight line with a slope.

\3. What is the form of the general equation of a straight line on a plane?

\4. What is the normal to the line?

\5. What does the equation with a slope for a straight line through a speciﬁed point

look like?

\6. Write the equation of a straight line through two speciﬁed points.

\7. How is the angle between two lines computed?

\8. Write intercept form of the equation of a straight line.

\9. Deﬁne the deviation of an arbitrary point from a given line.

\10. For solution of what problem is it convenient to use the normal form of the

equation of a line?

\11. How can the set of points of the segment M M be speciﬁed with the help of a

1

2

parameter?

**Problems**

**7.1.** Find the intersection point of the lines 2x − 3y + 4 = 0 and 4x + y − 6 = 0.

**7.2.** The sides of the triangle lie on the lines 5x − y + 12 = 0, x + y + 3 = 0

and 4x + 3y − 6 = 0. Find the coordinates of the vertices of this triangle.

**7.3.** The coordinates of the vertices of a triangle are (5, −4), (6, −6) and

(−15, 4). Find the equations of its sides.

**7.4.** Show that the area of a triangle with the vertices (x , y ), (x , y ) and

1

1

2

2

(x3, y3) is equal to




1

x1 y1

1


S = abs x y 1 .


(7.44)

` `2

2

2



1

x3 y3

**7.5.** The sides of the triangle lie on the lines x + y + 1 = 0, x + 2y − 3 = 0 and

4x − 3y − 2 = 0. Compute the area of this triangle.





Problems

291

**7.6. Median** of a triangle is the segment that connects its vertex with the

midpoint of the opposite side. Set up the equations of the lines on which

the medians of the triangle ABC lie, if A(1, 2), B(4, −3), C(6, 6).

**7.7.** Compute the distance from the point T (1, 7) to the line through A(−3, −20)

and B(4, 17).

**7.8.** Compute the distance from the origin of coordinates to the line given by the

x − x0

x0

y − y0

= 0, where x , y are real numbers not equal to

y0

equation

zero.

\+

0

0

**7.9.** One of the sides of the square lies on the line x +3y +10 = 0. Find the area

of this square if the coordinates of one of its vertices are (−4, −4).

**7.10.** At what point do the lines speciﬁed by the equations x/a + y/b = 1 and

x/b + y/a = 1, where a, b = 0, intersect?

**7.11.** Find the angle between the lines 3x + 5y − 10 = 0 and −2x + y + 4 = 0.

**7.12.** Find the values of the parameters λ and μ at which the lines λx +6y −2 = 0

and 2x + 3y − μ = 0:

(1) have exactly one common point,

(2) coincide,

(3) are parallel.

**7.13.** Compute the distance between the parallel lines speciﬁed by the equations


Ax + By + C = 0 and Ax + By + C = 0, where C = C .

∗**7.14.** On what condition do the lines A x + B y + C = 0, A x + B y + C = 0,

1

1

1

2

2

2

..., A x + B y + C = 0 intersect at one point?

n

n

n

**7.15.** The line L passes through the point T (x , y ) at the angle α the abscissa

0

0

∗

axis. Write the equation of the line L that passes through the same point T0

at the angle α to the line L.

∗**7.16.** The sides of a triangle are speciﬁed by the equation A x + B y + C = 0,

i

i

i

where i = 1, 2, 3. Find the equation of

(a) median,

(b) altitude,

(c) bisector,

drawn to the third side.

**7.17.** Compute the area of a triangle intercepted by the line Ax + By + C = 0

from the quadrantal angle.

**7.18.** Find the equation of the line that passes through the point T (x , y ) and

0

0

intercepts from the quadrantal angle a triangle with an area equal to S. The

variables x and y are positive.

0

0

**7.19.** Assume that some line passing through the point T (x , y ) intercepts from

0

0

the quadrantal angle a right triangle. What is the least area of this triangle?

The variables x and y are positive.

0

0





292

7 Equation of a Straight Line on a Plane

∗**7.20.** The sides of a triangle are speciﬁed by the equation α x + β y + γ = 0,

i

i

i

where i = 1, 2, 3. Show that the area of this triangle can be calculated by

the formula:

1

2

S =

,

(7.45)

2 abs(   )

1

2

3




α1 β1 γ1


where  = 

,  are the cofactors of the element γ , i ∈ {1, 2, 3}.

α2 β2 γ2

i

i




α3 β3 γ3

**7.21.** Prove that the points T (−2, −8), T (18, 2) and T (3, −11/2) lie on the

1

2

3

same line.

**7.22.** For what values of the real parameter a do the points T (0, 1), T (a, 2) and

1

2

T3(3, a) lie on the same line?

**7.23.** The coordinates of a triangle are given: A(1, −1), B(2, 4), C(−8, −1). Set

up the equation of the line that passes through the vertex A parallel to the

side BC.

**7.24.** The coordinates of a triangle are given: A(−2, 0), B(2, 3), C(−1, −1). Set

up the equation of the line that passes through the vertex B parallel to the

side AC.

**7.25.** It is known about the point N that it lies on the ordinate axis, and the distance

√

from this point to N(−2, −5/2) is equal to d = 2 2. Find the coordinates

of the point N.

**7.26.** It is known that the area of the triangle is equal to S = 6 and its two vertices

have the coordinates (1, 1) and (−2, −3). Find the coordinates of the third

vertex of the triangle if this vertex lies on the abscissa axis.

**7.27.** It is known that the area of the triangle is equal to S = 10 and its two vertices

have the coordinates (−2, 3) and (−7, −1). Find the coordinates of the third

vertex of the triangle if this vertex lies on the ordinate axis.

**7.28.** Find the projection of the point (2, −13) on the line that passes through the

points (0, 2) and (2, −8).

**7.29.** Find the projection of the point (a, a) on the line that passes through the

points (1, 2a) and (2, 3a), if a is an arbitrary real number.

**7.30.** Write a program in Python that determines, by the segment endpoint

coordinates, in which coordinate quadrants it is located. In contrast to the

solution of the Example [7.5](#br297)[ ](#br297)on page [287](#br297), consider the full set of possible

cases, including the one when the segment endpoints can belong to the

coordinate axes.





Answers and Solutions

293

**Answers and Solutions**

[**7.1**](#br300)[** ](#br300)Answer: (1, 2).

[**7.2**](#br300)[** ](#br300)Answer: (−5/2, −1/2), (−30/19, 78/19), (15, −18).

[**7.3**](#br300)[** ](#br300)Solution.

Let us use the equation of a straight line through two given points ([7.12](#br290)):

y − y1

x − x1

\=

.

y2 − y1

x2 − x1

Substituting the coordinates of the points from the problem statement, we obtain the

equation of the triangle sides:

2x + y − 6 = 0, 2x + 5y + 10 = 0, 10x + 21y + 66 = 0.

[**7.4**](#br300)[** ](#br300)Solution.

Denote the triangle vertices (x , y ), (x , y ) and (x , y ) by A , A and A ,

1

1

2

2

3

3

1

2

3

respectively.

As is well known (see page [262](#br273)), the area of an arbitrary triangle can be

−− −→ −− −→

represented as half of the modulus of the vector product A A × A A :

1

2

1

3




1 −− −→ −− −→

S = |A1A2 × A1A3| =

1 

−

−

x2 x1 y2 y1


.


2

2

x − x y − y 

3

1

3

1

This expression can be rewritten in the equivalent form:




1

x1 y1

1


S = abs x y 1 .


` `2

2

2



1

x3 y3

Thus, the formula ([7.44](#br300)) is proved. It implies that the necessary and sufﬁcient

condition of the three points belonging to one line is that the respective third-order

determinant is equal to zero.

[**7.5**](#br300)[** ](#br300)Solution.

Solving the systems of equations:

⎧

⎨

⎧

⎨

⎧

⎨

x + y + 1 = 0,

x + 2y − 3 = 0;

x + y + 1 = 0,

4x − 3y − 2 = 0;

x + 2y − 3 = 0,

4x − 3y − 2 = 0,

⎩

⎩

⎩





294

7 Equation of a Straight Line on a Plane

we ﬁnd the coordinates of the vertices of the triangle: (−5, 4), (−1/7, −6/7),

(13/11, 10/11).

As is shown in Problem [**7.4**](#br300), the area of an arbitrary triangle A A A , whose

1

2

3

vertices have the coordinates (x , y ), (x , y ) and (x , y ), respectively, is equal to

1

1

2

2

3

3




1

x1 y1

1


S = abs x y 1 .


` `2

2

2



1

x3 y3

In our case,





−5

4

1




1


1

1156

77

578

77

S = abs −1/7 −6/7 1

` `= abs

\=

.


2

2

[](#br302)

[](#br302)13 11 10 11 1

/

/

Note. See Problem [**7.20**](#br302)[** ](#br302)for a general solution.

[**7.6**](#br300)[** ](#br300)Solution.

The abscissa and the ordinate of the midpoint of the segment with the endpoints

(x1, y1) and (x2, y2) are determined by the formulae xm = (x1 + x2)/2 and xm

\=

(y1 + y2)/2, respectively.

Find the midpoints of the sides: (5/2, −1/2), (7/2, 4), (5, 3/2).

Then, we apply the formula ([7.12](#br290)) and obtain the following equations of the

medians of the triangle ABC:

x + 8y − 17 = 0, 14x + y − 53 = 0, 13x − 7y − 36 = 0.

[**7.7**](#br301)[** ](#br301)Solution.

The general equation of a straight line through (−3, −20) and (4, 17) has the

form 37x − 7y − 29 = 0.

We obtain the normal equation of this line. The normalizing multiplier ([7.32](#br295)) is

equal to

1

1

μ = −√

sgn(−29) = √

.

372 + 72

1418

Thus, the equation in normal form is

37

7

29

√

x − √

y − √

= 0,

1418

1418

1418





Answers and Solutions

295

and the deviation of the point T (1, 7) from the line is equal to

37

7

29

41

δ = √

· 1 − √

· 7 − √

= −√

.

1418

1418

1418

1418

41

Therefore, the sought distance is equal to √

[**7.8**](#br301)[** ](#br301)Solution.

.

1418

Bring the equation of a line to normal form.

The normalizing multiplier is equal to

1

1

μ = −+

sgn(−2x0y0) = +

sgn(x0y0),

2

2

0

2

2

0

x + y

x + y

0

0

and, therefore, the equation of a line can be written in the form:

⎛

⎞

x0

y0

x0y0

⎝

\+

− 2

⎠ sgn

= 0

\+

x

\+

y

\+

(x y )

0

.

0

2

2

0

2

2

0

2

2

0

x + y

x + y

x + y

0

0

0

Compute the deviation from the origin of coordinates (0, 0):

x0y0

δ = −2+

sgn(x0y0).

2

2

0

x + y

0

The distance from the origin of coordinates to the line is equal to the absolute

2 abs(x y )

0

0

value of the deviation: +

[**7.9**](#br301)[** ](#br301)Solution.

.

2

2

0

x + y

0

1

3

10

The deviation from the point (−4, −4) to the line −√ x − √ y − √ = 0

10

10

10

,

2

is equal to δ = −3

.

5

,

2

Hence, the distance from the point to this line is equal to d = 3

; it coincides

5

with the length of the side of the square.

The area of the square is S = d2 = 18/5.





296

7

Equation of a Straight Line on a Plane

[**7.10**](#br301)[** ](#br301)Solution.

The system of equations:

⎧

⎨

x/a + y/b = 1,

x/b + y/a = 1,

⎩

for a, b = 0 has the unique solution x = y = ab/(a + b).

$

%

ab

ab

Therefore, the lines intersect at the point

,

.

a + b a + b

[**7.11**](#br301)[** ](#br301)Solution.

Take the formula ([7.19](#br292)) in order to ﬁnd the tangent of the angle between the lines

speciﬁed in the general form. Substitute into it the values A = 3, B = 5, A = −2

1

1

2

and B = 1, and we obtain

2

A2B1 − A1B2

A1A2 + B1B2

tan α =

= 13.

Therefore, the angle between the lines is α = arctan 13.

[**7.12**](#br301)[** ](#br301)Solution.

Consider the system of equations:

⎧

⎨

λx + 6y = 2,

2x + 3y = μ.

⎩

Using the bordering minor method (see page [64](#br78)), we ﬁnd the ranks of the system

matrix and the augmented matrix:

⎡

⎤

λ 6

1, if λ = 4,

2, if λ = 4;

rk ⎣ ⎦ =

2 3

⎡

⎤

⎡

⎤

λ 6 2

2 3 μ

1 6

2

1, if μ = 1,

2, if μ = 1.

rk ⎣

⎦ = rk ⎣

⎦ =

0 0 μ − 4

Therefore:

(a) at λ = 4, μ = 1, the system has the unique solution, and the lines intersect

exactly at one point;

(b) at λ = 4, μ = 1, the system has an inﬁnite set of solutions, and the lines

coincide;

(c) at λ = 4, μ = 1, the system has no solution, and the lines are parallel.





Answers and Solutions

297

[**7.13**](#br301)[** ](#br301)Solution.

Find the deviation of each line from the origin of coordinates:

1

1




δ1 = −√

Csgn(C), δ2 = −√

C sgn C .

A2 + B2

A2 + B2

Then, as is easy to see, the distance d between the parallel planes is equal to the

absolute value of the difference of the deviations:


1

1



d = abs(δ1 − δ2) = abs −√

Csgn(C) + √

C sgn C

A2 + B2

A2 + B2

abs(C − C)

= √

.

2

A

2 +

B

[**7.14**](#br301)[** ](#br301)Answer: the criterion of intersection of n lines at one point is the equality of

the ranks of the two matrices:

⎡

⎤

⎡

⎤

A1 B1

A1 B1 C1

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

⎢A2 B2 ⎥

⎢A2 B2 C2 ⎥

and

.

⎢

⎥

⎢

⎥

⎢

⎥

⎢

⎥

. . . . . . .

. . . . . . . . . . .

⎣

⎦

⎣

⎦

A

B

n

A B

C

n n

n

n

[**7.15**](#br301)[** ](#br301)Solution.

The equation of the line L∗ that passes through the point T (x , y ) has the form

0

0

y − y0 = k(x − x0). In this equation, k is the unknown slope.

In order to ﬁnd the value of k, let us use its property: k = tan α∗, where α∗ is the

angle of inclination of L∗ relative to the abscissa axis.

Since L∗ passes at the angle α to the line L, then the two options arise: α∗ =

α −α and α

∗ =

α

\+

α

. Write these equations in the form of a common equality:

α∗ = α ± α.

By the formulae of tangent of sum and difference of two angles [(](#br418)[B.13](#br418)) and ([B.14](#br418))

on page [412](#br418), we have

tan α ± tan α

k = tan(α ± α) =

.

1 ∓ tan α tan α

We ﬁnally obtain the equation of the line L∗:

tan α ± tan α

y − y0 =

(x − x0).

1 ∓ tan α tan α





298

7 Equation of a Straight Line on a Plane

[**7.16**](#br301)[** ](#br301)Answer:












A2 B2

A3 B3

(a) (A x + B y + C ) 

` `= (A x + B y + C ) 

;

1

1

1 

2

2

2 

A B 

A B 

3

3

1

1

(b) (A x + B y + C )(A A + B B ) = (A x + B y + C )(A A + B B );

1

1

1

2

3

2

3

2

2

2

1

3

1 3

A1x + B1y + C1

A2x + B2y + C2

(c)

\+

= −s

\+

,

2

2

2

2

2

A + B

A + B

1

1

2

⎛



⎞






A1 B1 A2 B2

where s = sgn ⎝



⎠.



A B  A B 

3

3

3

3

[**7.17**](#br301)[** ](#br301)Solution.

Denote the intersection points of the line Ax + By + C = 0 with the coordinate

C

C

B

axes by P(x , 0) and Q(0, y ), where x = − , y = − . The coordinates x0

0

0

0

0

A

and y in the absolute value are equal to the lengths of the cathetuses of the right

0

triangle POQ lying on the axes Ox and Oy, respectively. The area of this triangle

is equal to the half of the product of the cathetuses:



1

1

2

C

A

C

B

C2

S = x0y0 =

−

−

\=

.

2

2AB

[**7.18**](#br301)[** ](#br301)Solution.

Write the equation of the line that passes through the point (x , y ): y − y =

0

0

0

k(x − x0), where k < ∞ is the slope.

The case k → ∞ does not require separate consideration, since in that case the

line will not intercept the triangle from the quadrantal angle.

Find the coordinates of the points of intersection of the line with the coordinate

axes:

y0

with the axis Ox: y = 0, −y = k(x − x ), x = x − , where abs(x∗) is the

∗

∗

0

0

0

k

length of the cathetus lying on the axis Ox;

with the axis Oy: x = 0, y∗ − y = −kx , y∗ = y − kx , where abs(y∗) is the

0

0

0

0

length of the cathetus lying on the axis Oy.

The area of such a triangle is equal to the half of the product of the cathetuses:

1

1

y 

1

(y − kx )2 

0

0

0

S = abs(x y ) S

∗

∗ ,

\=

x0

−

(y0 kx0)

−

\=

abs

.

2

2

k

2

−k

Let us express the variable k:

2

2

0

2

k x − 2k(x0y0 − S) + y = 0. The solution of this square equation leads to two

0

possible values of k:

x0y0 − S ±

√

k1,2 =

S(S − 2x0y0).

2

x

0





Answers and Solutions

299

We obtain the sought equation of the line:

2

√

3

x0y0 − S ± S(S − 2x0y0)

y − y0 =

(x − x0).

2

x

0

[**7.19**](#br301)[** ](#br301)Solution.

As is shown in the previous problem, the area of the triangle S depends on the

$

2 %

1

(y − kx )

0

0

slope of the line k as follows: S(k) = abs

.

2

−k

0

For the points T (x , y ), whose coordinates x and y are positive, the equality

0

0

0

k < 0 is fulﬁlled, i.e. in this case the line forms an obtuse angle with the axis Ox.

In order to ﬁnd the minimal value of the function, let us compute the points at

2

0

2

2

0

d S(k)

y

− k x

which the derivative

\=

is equal to zero.

2

d k

k

y0

The condition k < 0 is satisﬁed by the value k∗ = − . The point k∗ is the

x0

2

∗

d S(k )

2 2

y

0

∗ 3

minimum point, since the second derivative is

= −

\> 0.

d k

(k )

Thus, the least value of the area of the triangle is equal to

Smin = S(k∗) = 2x0y0.

[**7.20**](#br302)[** ](#br302)Solution.

Compute the coordinates of the intersection points of the line pairs. Taking into

account that the area of the triangle is expressed in the form of a half of the modulus

of the vector form of the vectors that from both sides, we obtain


β1γ2 − β2γ1 α2γ3 − α3γ2

α3γ1 − α1γ3

α1β3 − α3β1

S =

−

α1β2 − α2β1 α3β2 − α2β3



β2γ3 − β3γ2 α3γ1 − α1γ3

α1γ2 − α2γ1

\+

−

α2β3 − α3β2 α1β3 − α3β1

α2β1 − α1β2

β3γ1 − β1γ3 α1γ2 − α2γ1

α2γ3 − α3γ2

α3β2 − α2β3

\+

−

.

α3β1 − α1β3 α2β1 − α1β2

Reduce the fractions to a common denominator. After simple but somewhat

cumbersome algebraic transformations, we arrive at the formula:

(α1(β2γ3 − β3γ2) + α2(β3γ1 − β1γ3) + α3(β1γ2 − β2γ1))2

S =

.

(α1β2 − α2β1)(α2β3 − α3β2)(α3β1 − α1β3)





300

7 Equation of a Straight Line on a Plane

As is easy to see, the obtained expression can be presented as

1

2

S =

,

2 abs(   )

1

2

3




α1 β1 γ1


where  = 

,  are the cofactors of the elements γ , i ∈ {1, 2, 3}.

α2 β2 γ2

i

i




α3 β3 γ3

[**7.21**](#br302)[** ](#br302)Solution.

Let us draw a line through the points T and T (see the formula ([7.12](#br290))). The

1

2

slope of this line is k = 1/2. Then, the line T T has the slope k = 1/2. Since

1

3

k = k

, then the points

T1 T2 T3

, and lie on the same line.

[**7.22**](#br302)[** ](#br302)Solution.

T h e f i r s t m e t h o d

Let the equation of the line passing through the three points T , T and T have

1

2

3

the form y = kx +b. Having substituted the coordinates of each of these points into

the equation of the line, we obtain the system of relatively unknown variables k and

b:

⎧

⎪

= 1

⎪

b

,

⎨

ak + b = 2,

3k + b = a.

⎪

⎪

⎩

The condition of deﬁniteness of this system (i.e. the uniqueness of its solution)

leads to the square equation a2 − a − 3 = 0.

Therefore, the points T , T and T lie on the same line at the two values of the

1

2

3

1

√

1

√

parameter a: a = (1 + 13) and a2 = (1 − 13).

1

2

2

T h e s e c o n d m e t h o d

Let us use the consequence of the formula ([7.44](#br300)) from Problem [**7.4**](#br300): the criterion

of the three points belonging to one line is that the third-order determinant is equal

to zero:





0 1 1

2 1





` `= 0

a

.

3 1

a

1

2

√

The obtained equation has two roots: a1,2

\=

(1 ± 13).

Note. The necessary and sufﬁcient condition for the three points T , T and T

1

2

3

−−→

1

−−→

1 3

to lie on the same line is collinearity of the vectors T T and T T . In view of this,

2

there exists one more method of solving this problem, which is based on checking

−−→ −−→

whether the vector product T T ×T T is equal to zero. Of course, different solution

1

2

1 3

methods result in the same answer.





Answers and Solutions

301

[**7.23**](#br302)[** ](#br302)Solution.

The slope of the sought line coincides with the slope of the line BC. The equation

1

of the line BC has the form y = x + 3 (see the formula ([7.12](#br290))). Then, use the

2

formula ([7.10](#br290)) for the line that passes through a given point:

y − y1 = k(x − x1),

(7.46)

1

where k = , x = 1, y = −1.

1

1

2

Substituting the numeric values, we obtain the equation of the line that passes

through the vertex A parallel to the side BC: x − 2y − 3 = 0.

[**7.24**](#br302)[** ](#br302)Answer: x + y − 5 = 0.

[**7.25**](#br302)[** ](#br302)Solution.

Since the point N lies on the ordinate axis, its coordinates are equal to (0, y),

where y is an unknown value. The distance d between the points N and N is equal

to

\+

\+

d = (0 − (−2))2 + (y

− −5 2 2 = 4 + + 5 2 2

(

/ ))

(y

/ ) .

Thus, we obtain the equation relative to the variable y:

\+

√

(0 − (−2))2 + (y

(

/ ))2 = 2 2,

− −5 2

which has the solutions y = −1/2 and y = −9/2. Therefore, the coordinates of

1

2

the point N are equal to (0, −1/2) or (0, −9/2).

[**7.26**](#br302)[** ](#br302)Solution.

By the triangle area formula expressed by the coordinates of its vertices (1, 1),

(−2, −3) and (x, 0) (see ([7.44](#br300)) on page [290](#br300)), we obtain S = abs(4x − 1).

According to the problem statement, S = 6, hence abs(4x − 1) = 13/4.

Therefore, the coordinates of the vertices of the triangle are equal to (−5/4, 0)

or (7/4, 0).

[**7.27**](#br302)[** ](#br302)Solution.

The coordinates of the third vertex are (0, y).

The area of the triangle is equal to





−2 3 1


1


1

2

S = abs −7 −1 1

` `= abs 23 − 5 = 10

(

y)

,


2

` `0

1

y

hence y = 13/5 or y = 33/5.





302

7 Equation of a Straight Line on a Plane

The coordinates of the third vertex of the triangle are equal to (0, 13/5) or

(0, 33/5).

[**7.28**](#br302)[** ](#br302)Solution.

Let A(0, 2), B(2, −8). The sought projection of the point is K(2, −13).

The projection of the point is the foot of the perpendicular to the line AB. Then,

the orthogonality property for the line AB and the perpendicular from the point K:

k1 · k2 = −1 is fulﬁlled.

Write the system of equations relative to the coefﬁcients k and b for the line

1

1

A B⎧:

⎨

2 = b1,

⎩

8 = 2k + b ,

1

1

From this system, we obtain that b = 2, k = −5. Then, k = 1/5.

1

1

2

Substitute k into the equation of the line for the perpendicular from the point K:

2

−13 = 2 · 1/5 + b , hence b = −67/5.

2

2

Compute the coordinates of the point (x , y ), at which the lines intersect:

0

0

1/5x − 67/5 = −5x + 2, x = 77/26, y = −333/26.

0

0

0

0

[**7.29**](#br302)[** ](#br302)Solution.

Let A(1, 2a), B(2, 3a), K(a, a).

Projection of a point is a foot of a perpendicular to the line AB. Then, the equality

is fulﬁlled for the line AB and the perpendicular from the point K: k · k = −1.

1

2

Write the system of equations relative to the coefﬁcients k and b for the line

1

1

A B⎧:

⎨

2a = k + b ,

1

1

⎩

3a = 2k + b .

1

1

From this system, we obtain that b = a, k = a. Then, k = −1/a.

1

1

2

Substitute k into the equation of the line for the perpendicular from the point K:

2

a = a(−1/a) + b2, hence b2 = a + 1.

The coordinate of the projection of the point K satisﬁes the equation:

a

ax0+a = −1/ax0+b2, ax0+a = −x0/a+a+1, x0(a+1/a) = 1, x0 =

.

.

a

2 + 1

a

a2 + 1

1

Let us express the ordinate of the projection: y = −

+a+1 = a+

0

a2 + 1


a

a

The sought projection has the coordinates

, a +

.

a2 + 1

a2 + 1

[**7.30**](#br302)[** ](#br302)Solution.

The suggested solution generally repeats the approach discussed in Example [7.5](#br297).

Note that in order to study the full set of possible cases of mutual arrangement of

the segment endpoints and the coordinate axes, the integer variable neighbor

is additionally used. It plays an important role for the location of the segment

illustrated in Fig. [7.8](#br313). Here, one of the segment endpoints, namely P2, is located

on the coordinate axis, and into the variable neighbor will be written the number

of the quadrant where the segment points from the small neighborhood P2 lie.





Answers and Solutions

303

y

II

I

P2

x

O

P1

III

IV

**Fig. 7.8** To Problem [**7.30**](#br302). The segment P1P2 lies in the second and third quadrants,

get\_quadrant(p1) = 3, get\_quadrant(p2) = 0, neighbor = 2

After performing all checks, into the answer will be written the numbers of the

quadrants within which the segment points fall.

class Point:

def \_\_init\_\_(self, x, y):

self.x = x

self.y = y

def get\_quadrant(p):

if p.x > 0 and p.y > 0:

return 1

elif p.x < 0 and p.y > 0:

return 2

elif p.x < 0 and p.y < 0:

return 3

elif p.x > 0 and p.y < 0:

return 4

else:

return 0

def get\_quadrants\_general(p1, p2):

p1\_quad = get\_quadrant(p1)

p2\_quad = get\_quadrant(p2)





304

7 Equation of a Straight Line on a Plane

is\_adjacent = abs(p1\_quad - p2\_quad) % 2 == 1

if p1\_quad == 0 and p2\_quad == 0:

mid = Point((p1.x + p2.x) / 2, (p1.y + p2.y) / 2)

mid\_quad = get\_quadrant(mid)

return [] if mid\_quad == 0 else [mid\_quad]

elif p1\_quad == 0:

if p1.x

p2.x < 0:

\*

neighbour = 3 - p2\_quad \

if p2\_quad <= 2 else 7 - p2\_quad

return [p2\_quad, neighbour]

if p1.y

p2.y < 0:

\*

neighbour = 5 - p2\_quad

return [p2\_quad, neighbour]

return [p2\_quad]

elif p2\_quad == 0:

if p1.x p2.x < 0:

\*

neighbour = 3 - p1\_quad if p1\_quad <= 2 \

else 7 - p1\_quad

return [p1\_quad, neighbour]

if p1.y

p2.y < 0:

\*

neighbour = 7 - p1\_quad

return [p1\_quad, neighbour]

return [p1\_quad]

elif is\_adjacent:

return [p1\_quad, p2\_quad]

elif p1\_quad == p2\_quad:

return [p1\_quad]

else:

b = (p1.y

p2.x - p1.x

p2.y) \

\*

\*

/ (p2.x - p1.x)

if b == 0:

return [p1\_quad, p2\_quad]

elif p1\_quad == 1 or p2\_quad == 3:

quadrant = 2 if b > 0 else 4

return [p1\_quad, p2\_quad, quadrant]





Answers and Solutions

305

else:

quadrant = 1 if b > 0 else 3

return [p1\_quad, p2\_quad, quadrant]





**Chapter 8**

**Equation of a Plane in Space**

**8.1 Equation of a Plane That Is Orthogonal to the Speciﬁed**

**Vector and Passes Through the Speciﬁed Point**

Assume that it is known that the plane π is orthogonal to the vector **n** = (A, B, C)

and passes through the point T (x , y , z ). Take an arbitrary point T (x, y, z) on the

0

0

0

0

−−→

0

plane π. The vector T T belongs to the plane π. From the condition of orthogonality

of the vector **n** of the plane π follows that the vector

−−→

T0T = (x − x0, y − y0, z − z0)

(8.1)

is orthogonal to the vector **n**.

Relying on the property of the scalar product of orthogonal vectors, we can write

−−→

**n** · T T = 0.

(8.2)

0

This equation is called the **vector equation of a plane** [[8](#br420)[\].](#br420)

Rewritten in coordinate form

A(x − x0) + B(y − y0) + C(z − z0) = 0,

(8.3)

this equation is called the **equation of a plane that is orthogonal to the vector**

**n** = (A, B, C) **and passes through the point** T (x , y , z ).

0

0

0

0

© Springer Nature Switzerland AG 2021

307

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_8>





308

8

Equation of a Plane in Space

**8.2 General Equation of a Plane**

Equation of the ﬁrst degree

Ax + By + Cz + D = 0,

(8.4)

in which A, B, C and D are arbitrary real constants such that out of the coefﬁcients

A, B and C at least one is other than zero, is referred to as the **general equation of**

**a plane**.

A general equation ([8.4](#br317)) is referred to as **complete** if all its coefﬁcients are other

than zero. If at least one of the mentioned coefﬁcients is equal to zero, the equation

is referred to as **incomplete**.

Consider the possible types of incomplete equations.

(1) If D = 0, then the equation Ax + By + Cz = 0 determines the plane that

passes through the origin of coordinates.

(2) If A = 0, then the equation By + Cz + D = 0 determines the plane

parallel to the axis Ox, since the normal vector of this plane **n** = (0, B, C) is

perpendicular to the axis Ox.

(3) If B = 0, then the equation Ax + Cz + D = 0 determines the plane, parallel

to the axis Oy, since its normal vector **n** = (A, 0, C) is perpendicular to the

axis Oy.

(4) If C = 0, then the equation Ax + By + D = 0 determines the plane parallel

to the axis Oz, since for this axis perpendicular is the normal vector with the

coordinates (A, B, 0).

(5) If A = B = 0, then the equation Cz + D = 0 determines the plane parallel to

the coordinate plane xOy.

(6) If A = 0 and C = 0, then the equation By + D = 0 determines the plane,

parallel to the coordinate plane xOz.

(7) If B = 0 and C = 0, then the equation Ax + D = 0 determines the plane,

parallel to the coordinate plane yOz.

(8) If A = 0, B = 0 and D = 0, then the equation of the plane Cz = 0 determines

the coordinate plane xOy.

(9) If A = 0, C = 0 and D = 0, then the equation of the plane By = 0 determines

the coordinate plane xOz.

(10) If B = 0, C = 0 and D = 0, then the equation of the plane Ax = 0 determines

the coordinate plane yOz.





8.3 Intercept Form of the Equation of a Plane

309

**8.3 Intercept Form of the Equation of a Plane**

Consider the general equation of the plane Ax + By + Cz + D = 0.

Assume that all the coefﬁcients A, B, C and D are other than zero. Then this

equation can be written in the form:

x

y

z

\+

\+

= 1.

(8.5)

(−D/A) (−D/B) (−D/C)

D

D

B

D

Let us introduce the notations: a = − , b = − , c = − . Then Eq. ([8.5](#br318)) will

A

C

be reduced to the following form:

x

y

z

c

\+

\+

b

= 1.

(8.6)

a

This is the **intercept form of the equation of a plane**.

In Eq. ([8.6](#br318)) the numbers a, b and c have simple geometric meaning: they are

equal in absolute value to the lengths of the segments (intercepts) that the plane

intercepts on the coordinate axes Ox, Oy and Oz, respectively (see Fig. [8.1](#br318)). The

plane passes through the points (a, 0, 0), (0, b, 0), (0, 0, c).

z

c

b

y

a

x

**Fig. 8.1** The intercepts that are intercepted by the plane on the coordinate axes





310

8 Equation of a Plane in Space

**8.4 Normal Equation of a Plane**

Consider the plane shown in Fig. [8.2](#br319).

−→

Assume that p is the length of the vector OP; α, β, γ are the angles between the

unit vector **n** and the coordinate axes; Q is the arbitrary point on the plane with the

coordinates (x, y, z).

−−→

It is obvious that the projection of the vector OQ on the direction **n** is equal to p:

−−→

Pr OQ = p,

(8.7)

(8.8)

**n**

−−→

−−→

Pr OQ =

·

,

OQ **n**

|**n**| = 1.

**n**

|**n**|

Therefore

−−→

OQ · **n** = x cos α + y cos β + z cos γ = p.

(8.9)

We have obtained the **normal equation of a plane**. The variables cos α, cos β, cos γ

are called the **direction cosines** of the vector **n**.

Take the general equation of a plane

Ax + By + Cz + D = 0,

(8.10)

where D = 0.

**Fig. 8.2** To the derivation of

the normal equation of a

plane

z

y

P

**n**

Q(x, y, z)

O

x





8.5 Equation of a Plane That Passes Through the Speciﬁed Point Parallel to. . .

311

The normalizing factor is calculated by the formula:

1

μ = −√

sgn(D)

(8.11)

A2 + B2 + C2

(cf. the formula ([7.32](#br295))).

If we multiply ([8.10](#br319)) by the normalizing factor μ, then as a result we obtain the

normal equation of the plane:

μ(Ax + By + Cz + D) = 0.

(8.12)

Note If the condition D = 0 is met, then the plane passes through the origin of

coordinates, and the normalizing factor can be taken with an arbitrary sign: μ =

1

± √

.

A2 + B2 + C2

**8.5 Equation of a Plane That Passes Through the Speciﬁed**

**Point Parallel to the Two Speciﬁed Vectors**

Let the plane π be parallel to the vectors **a** = (k , l , m ) and **a** = (k , l , m )

1

1

1

1

2

2

2

2

and pass through the point T (x , y , z ). Further, let T (x, y, z) be an arbitrary point

0

0

0

0

−−→

on the plane. Then the vectors **a** , **a** and T T are **coplanar**. Therefore,

1

2

0

−−→

(T0T × **a**1) · **a**2 = 0,

(8.13)

(8.14)





− x y − y z − z

x

0

0

0



` `= 0

k1

l1

m1 



k2

l2

m2

or


















l1 m1

k1 m1

k1 l1

(x − x0)

` `−

(y y0)

−

` `+

(z z0)

−

` `= 0

.

(8.15)






l m 

k m 

k l 

2

2

2

2

2

2

After expanding the second order determinants and introducing the appropriate

notation, we obtain the general equation of the plane.





312

8 Equation of a Plane in Space

**8.6 Equation of the Plane That Passes Through the Three**

**Speciﬁed Points**

Given are the following points: T (x , y , z ), T (x , y , z ) and T (x , y , z ).

1

1

1

1

2

2

2

2

3

3

3

3

−−→ −−→

−−→

1 3

Take an arbitrary point T (x, y, z) and construct the vectors T T , T T and T T .

1

1

2

They are coplanar, therefore




− x1 y − y1 z − z

− x y − y z − z

1 

` `x



` `= 0

(8.16)

x2

1

2

1

2

1

.



−

−

−

x3 x1 y3 y1 z3 z1

The obtained equation is the **equation of a plane that passes through the three**

**speciﬁed points**.

**8.7 Angle Between Two Planes**

Consider the planes speciﬁed by the equations:

A1x + B1y + C1z + D1 = 0,

A2x + B2y + C2z + D2 = 0.

(8.17)

(8.18)

For the given planes, construct the normal vectors **n** = (A , B , C ) and **n** =

1

1

1

1

2

(A2, B2, C2). Therefore, the angle ω between the planes will be determined from

the relation:

**n** · **n**

A A + B B + C C

1

2

1

2

1

2

1 2

cos ω =

= +

\+

.

(8.19)

|**n** ||**n** |

1

2

2 + 2 +

2

1

2 + 2 +

2

2

A

B

C

A

B

2

C

1

1

2

If **n** · **n** = 0, then the vectors **n** and **n** are orthogonal. Hence,

1

2

1

2

A1A2 + B1B2 + C1C2 = 0 is the **condition of orthogonality of planes**.

(8.20)

A1

A2

B1

B2

C1

C2

But if the equalities

\=

\=

are valid, then the vectors **n** and **n** are

1

2

collinear, and this will be the **condition of parallelism of planes**.





8.9 Pencil of Planes

313

**8.8 Distance from a Point to a Plane**

The concept of **deviation of the point** T (x , y , z ) **from the plane** Ax + By +

0

0

0

0

Cz + D = 0 is introduced similarly to the relation ([7.37](#br296)):

Ax0 + By0 + Cz0 + D

δ = −sgn(D)

√

.

(8.21)

2 + 2 +

B

C

2

A

**The distance** d **from the point** T0 **to the plane** is determined as the absolute

value of the deviation d = abs(δ).

If the plane is speciﬁed in the normal form, then the distance d is determined as

d = abs(cos α · x0 + cos β · y0 + cos γ · z0 − p),

where cos α, cos β, cosγ are the direction cosines.

(8.22)

**8.9 Pencil of Planes**

Assume that two planes are speciﬁed by the equations:

A1x + B1y + C1z + D1 = 0,

(8.23)

A2x + B2y + C2z + D2 = 0.

If these planes are neither parallel nor coincide, then they intersect on some straight

line.

It is obvious that for any real constants λ and μ, the plane determined by the

equation

λ(A1x + B1y + C1z + D1) + μ(A2x + B2y + C2z + D2) = 0

(8.24)

will also pass through this line, because all the points governed by Eqs. ([8.23](#br322)) satisfy

Eq. ([8.24](#br322)) as well. The same equation speciﬁes all the planes that pass through a

common line.

A collection of planes passing through the same straight line is called the **pencil**

**of planes**.

Example 8.1 Find the equation of the plane that passes through the point

T (4, −1, 2) and a straight line that is the intersection of the planes x+3y−z−5 = 0

and −2x + y + z + 4 = 0.





314

8 Equation of a Plane in Space

**Solution** Write the equation of the pencil of planes and ﬁt λ and μ so that the

required plane passes through the point T :

λ(x + 3y − z − 5) + μ(−2x + y + z + 4) = 0,

λ(4 + 3 · (−1) − 2 − 5) + μ(−2 · 4 + (−1) + 2 + 4) = 0,

− 6λ − 3μ = 0,

(8.25)

(8.26)

(8.27)

(8.28)

2λ + μ = 0.

For example, take the values λ = 1 and μ = −2. In this case, we obtain the answer:

(x + 3y − z − 5) + (−2)(−2x + y + z + 4) = 0, or

5x + y − 3z − 13 = 0.

(8.29)

(8.30)

**Review Questions**

\1. Write the equation of a plane orthogonal to a speciﬁed vector and passing

through a speciﬁed point.

\2. Deﬁne the general equation of a plane?

\3. Write the intercept form of the equation of a plane.

\4. For solution of what problem is it convenient to use the normal form of the

equation of a plane?

\5. How are the directing cosines of the vector **a** computed?

\6. Write the equation of a plane that passes through a speciﬁed point parallel to

two speciﬁed vectors.

\7. Write the equation of a plan that passes through three speciﬁed points.

\8. How is the angle between two planes computed?

\9. Deﬁne the deviation of an arbitrary point from a given plane.

\10. What is pencil of planes?

**Problems**

**8.1**. Set up the equation of the plane that passes through the origin of coordinates,

if it has the normal vector **n** = (1, 2, −3).

**8.2**. Set up the equation of the plane that passes through the point T (−1, 0, 2)

and has the normal vector **n** = (−3, −2, 0).





Answers and Solutions

315

**8.3**. Find the equation of the plane that passes through the points T (2, −1, 0)

1

and T (−5, 1, 1) parallel to the vector **a** = (0, −1, −7).

2

**8.4**. Find the equation of the plane that passes through the point T (2, −1, 0)

0

parallel to the vectors **a** = (3, 5, −8) and **a** = (4, 6, −7).

1

2

**8.5**. Find the equation of the plane that passes through the point T (1/2, 1/2, 1/2)

0

parallel to the vectors **a** = (0, 1, −1) and **a** = (1, 1, 10).

1

2

**8.6**. Find the lengths of the segments intercepted by the plane 3x+4y+5z−12 =

0 on the coordinate axes.

**8.7**. What is the distance from the point A(1, 2, 9) to the plane x +y −2z−17 =

0?

**8.8**. Does the plane −2x + 2y − z − 1 = 0 intersect the segment P P , if the

1

2

segment endpoint coordinates are as follows: P (−5, −5, −5), P (8, 8, 8)?

1

2

**8.9**. Compute the distance between the parallel planes speciﬁed by the equations

Ax + By + Cz + D = 0 and Ax + By + Cz + D

` `= 0, where

D

\=

D.

∗**8.10.** On what condition do the three planes A x + B y + C z + D = 0, A x +

1

1

1

1

2

B2y + C2z + D2 = 0 and A3x + B3y + C3z + D3 = 0 intersect exactly at

one point? Find the coordinates of this point.

**8.11**. Find the volume of a tetrahedron intercepted by the plane Ax + By + Cz +

D = 0 from the quadrantal angle.

**8.12**. On the axis Oz ﬁnd the points equidistant from the two planes x − y + z −

10 = 0 and x + y − z + 8 = 0.

∗**8.13.** Compute the volume of a tetrahedron whose vertices are located at the points

with the coordinates (x , y , z ), (x , y , z ), (x , y , z ) and (x , y , z ).

1

1

1

2

2

2

3

3

3

4

4

4

**Answers and Solutions**

[**8.1**](#br323)[** ](#br323)Solution.

Use the formula ([8.3](#br316)) that expresses the equation of the plane that passes through

the point A (x , y , z ) perpendicular to the vector **n** = (n , n , n ):

0

0

0

0

1

2

3

n1(x − x0) + n2(y − y0) + n3(z − z0) = 0.

Substitute the coordinates of the point O(0, 0, 0): (x−0)+2(y−0)−3(z−0) = 0.

Hence, the equation of the sought plane has the form x + 2y − 3z = 0.

[**8.2**](#br323)[** ](#br323)Solution.

Substitute into the formula ([8.3](#br316)) the coordinates of the point T (−1, 0, 2) and the

vector **n** = (−3, −2, 0); we obtain the equation of the plane:

(−3)(x − (−1)) + (−2)(y − 0) + 0(z − 2) = 0,

or

3x + 2y + 3 = 0.





316

8 Equation of a Plane in Space

[**8.3**](#br324)[** ](#br324)Solution.

Select an arbitrary point T (x, y, z) on the sought plane. According to the problem

−−→ −−→

statement, the vectors T T , T T and **a** are coplanar, therefore, their scalar triple

1

1

2

product is equal to zero:

−−→ −−→

(T1T , T1T2, **a**) = 0.

Use the formula ([6.33](#br274)):




− 2 y + 1 z

x

−−→ −−→


(T1T , T1T2, **a**) = −7

2

1

` `= −13 − 49 + 7 − 23 = 0

x

y

z

.





0

−1 7

Then, the equation of the plane that passes through the points T and T parallel to

1

2

the vector **a** can be presented in the form 13x + 49y − 7z + 23 = 0.

[**8.4**](#br324)[** ](#br324)Solution.

Consider an arbitrary point T (x, y, z) on the sought plane. The scalar triple

−−→

product of (**a** , **a** , T T ) is equal to zero because of coplanarity of these three

1

2

1

vectors.

Having computed the scalar triple product, we obtain




3

4

5

6

−8

−7

z


−−→

(**a**1, **a**2, T0T ) =



` `= 13 − 11 − 2 − 37 = 0

x

y

z

.




` `− 2 + 1

x

y

Hence, the equation of the plane that passes through the point T parallel to the

0

vectors **a** and **a** can be presented in the form 13x − 11y − 2z − 37 = 0.

1

2

[**8.5**](#br324)[** ](#br324)Solution.

Using an auxiliary point T with the coordinates T (x, y, z), similarly to the

solution of the previous problem, we obtain

−−→

(**a**1, **a**2, T0T ) = 0,





0

1

1

1

−1 


9

2


10 = 11 −

−

−

= 0


x

y

z

.


1

2

1

1

2


−

y − z −

2

x

As a result, the equation of the plane that passes through the point T parallel to the

0

vectors **a** and **a** has the form 22x − 2y − 2z − 9 = 0.

1

2





Answers and Solutions

317

[**8.6**](#br324)[** ](#br324)Solution.

Assume that the general equation of the plane Ax+By+Cz+D = 0 is speciﬁed,

and D = 0. Pass on to the intercept form of the equation of a plane, dividing both

sides of the equation by −D:

A

D

B

C

−

x − y − z = 1.

D D

D

D

D

The variables a = − , b = − and c = − are modulo equal to the lengths

A

B

C

of the segments intercepted by the plane on the coordinate axes Ox, Oy and Oz,

respectively (see the formula ([8.6](#br318))).

Having substituted the values of the coefﬁcients A = 3, B = 4, C = 5, D =

12

−12, we obtain a = 4, b = 3, c =

.

5

[**8.7**](#br324)[** ](#br324)Solution.

Write the equation of a plane in normal form:

1

1

\-

(x + y − 2z − 17) = √ (x + y − 2z − 17) = 0.

6

12 + 12 + (−2)2

Substitute the coordinates of the point from the problem statement into the normal

equation and ﬁnd the distance from this point to the plane:


1

32

d = abs √ (1 + 2 − 18 − 17) = √ .

6

6

[**8.8**](#br324)[** ](#br324)Solution.

The plane divides the space into two parts: −2x+2y−z−1 > 0 and −2x+2y−

z−1 < 0. If two endpoints of the segment are located in different parts of the space,

then it is obvious that the segment intersects the plane. Substitute the coordinates of

the points from the problem statement:

−2 · (−5) + 2 · (−5) − (−5) − 1 = 4 > 0,

−2 · 8 + 2 · 8 − 8 − 1 = −9 < 0.

Therefore, the points P and P are situated on the opposite sides of the plane, and

1

2

the segment P P intersects the plane −2x + 2y − z − 1 = 0.

1

2

[**8.9**](#br324)[** ](#br324)Solution.

Find the deviation of each plane from the origin of coordinates:

1

1



D sgn(D ).

δ1 = −√

Dsgn(D), δ2 = −√

A2 + B2 + C2

A2 + B2 + C2





318

8 Equation of a Plane in Space

Then the distance d between the parallel planes is equal to the absolute value of

the difference of these deviations:

d = abs(δ1 − δ2)

$

%

1

1



D sgn(D )

= abs − √

Dsgn(D) + √

A

2 +

B2 + C2

A2 + B2 + C2

abs(D − D)

= √

.

2 + 2 +

B

C

2

A

[**8.10**](#br324)[** ](#br324)Answer:

The condition of three planes intersecting at one point is that the determinant is

other than zero:




A1 B1 C1


1 = A B C

` `= 0

.

2

2

2




A3 B3 C3

The coordinates (x , y , z ) of the intersection point of these planes are

P

P

P












D1 B1 C1

A1 D1 C1

A1 B1 D1

1 

1 

1 

xP = −


,

yP

= −


,

zP

= −


.

D B C

2

2

2

A D C

2

2

2

A B D

2

2

2















D3 B3 C3

A3 D3 C3

A3 B3 D3

Note that if  = 0 and at least one second order minor of the matrix

⎡

⎤

A1 B1 C1

A2 B2 C2

A3 B3 C3

⎢

⎥

⎢

⎥ is other than zero, then all planes are parallel to the same line. But

⎣

⎦

if all the second order minors are zeroes, then the planes have the common line.

[**8.11**](#br324)[** ](#br324)Solution.

Pass on to the intercept form of the equation of a plane:

A

D

D

A

B

C

−

−

x − y − z = 1,

D D

D

D

= a, − = b, − = c,

B

C

where a, b and c are modulo equal to the lengths of the segments intercepted on the

coordinate axes by the plane and coinciding with the edges of the tetrahedron. The





Answers and Solutions

319

volume of the tetrahedron Vtetr and the volume of the parallelepiped Vpar are bound

as follows:

1

Vtetr = Vpar, where Vpar = abs(abc).

6

Substitute the values of a, b and c:


1

D3

Vtetr = abs

.

6

ABC

[**8.12**](#br324)[** ](#br324)Solution.

Find the normal equations of the planes:

1

√ (x − y + z − 10) = 0,

3

1

−√ (x + y − z + 8) = 0.

3

The coordinates of the point located on the axis Oz are (0, 0, z ), where z ∈ R. In

0

0

order to ﬁnd the distance from this point to the plane, substitute the coordinates into

Eqs. ([8.22](#br322)):

⎧

abs(z − 10)

⎪

0

⎪

√

\=

\=

⎨

d ,

1

3

abs(−z + 8)

⎪

0

⎪

√

⎩

d2.

3

Equate the distances:

abs(z − 10) = abs(−z + 8) ⇒ z = 9.

0

0

0

So, the problem statement is satisﬁed by a point with the coordinates (0, 0, 9).

[**8.13**](#br324)[** ](#br324)Solution.

Denote the vertices of the tetrahedron (x , y , z ) by A , respectively (i =

i

i

i

i

1, 2, 3, 4). The volume of the tetrahedron is one sixth part of the absolute value

−− −→ −− −→ −− −→

of the scalar triple product (A A , A A , A A ):

1

2

1

3

1

4




− x y − y z − z

x2

1

2

1

2

1

1

−− −→ −− −→ −− −→

1


V = abs(A1A2, A1A3, A1A4) = abs x − x y − y z − z


.

` `3

1

3

1

3

1

6

6



−

−

−

x4 x1 y4 y1 z4 z1





320

8 Equation of a Plane in Space

Note that this expression can be rewritten in equivalent form:




1

x y z

1

1

1




1

1

x2 y2 z2

V = abs 

` `.

6


x3 y3 z3 1





1

x4 y4 z4





**Chapter 9**

**Equation of a Line in a Space**

**9.1 Equation of a Line That Passes Through the Speciﬁed**

**Point Parallel to the Speciﬁed Vector**

Assume that the line L passes through the point T (x , y , z ) parallel to the vector

0

0

0

0

**a** = (k, l, m). Take an arbitrary point T (x, y, z) on the line and construct the vector

−−→

T0T = (x − x0, y − y0, z − z0), parallel to the line L and collinear with the vector

**a**. Then, we can write the equation

x − x0

y − y0

z − z0

m

\=

\=

.

(9.1)

k

l

This relation is referred to as the **canonical equation of a line that passes**

**through the speciﬁed point parallel to the speciﬁed vector**, and the vector

**a** = (k, l, m) is referred to as the **directing** vector.

From the canonical equation ([9.1](#br330)), we can easily derive the **parametric equation**

of such a line:

⎧

⎪

−

\=

⎪x x0 ku,

⎨

y − y0 = lu,

z − z0 = mu,

(9.2)

⎪

⎪

⎩

where u ∈ R is the **parameter** of the line.

Example 9.1 Let us ﬁnd the equation of the line that passes through the point

T (3, −1, 0) perpendicular to the plane x − 4y + 7z − 10 = 0.

© Springer Nature Switzerland AG 2021

321

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_9>





322

9 Equation of a Line in a Space

**Solution** The normal vector of the plane **n** = (1, −4, 7) will in this case coincide

with the directing vector for the line:

x − 3

y + 1

−4

z

\=

\=

.

(9.3)

1

7

Example 9.2 Let us ﬁnd the canonical equation of the line that is the intersection of

the planes determined by the equations −x − y + z + 2 = 0 and 2x + 4y − z = 0.

**Solution** The line is orthogonal to the normal vectors of each of the planes: **n** =

1

(−1, −1, 1), **n**2 = (2, 4, −1). Therefore, as the directing vector of the line, we can

take **a** = **n** × **n** .

1

2





` `**i**

**j**

**k** 


**a** = −1 −1 1

` `= −3 + − 2

**i**

**j**

**k**, **a**

(

, , ).

= −3 1 −2

(9.4)



` `2 4 −1

As the coordinates of the point that lies on the line, we select any solution of the

system

⎧

⎨

−x − y + z + 2 = 0,

2x + 4y − z = 0.

(9.5)

(9.6)

⎩

Let z = 0, then

⎧

⎨

−x − y = −2,

2x + 4y = 0,

⇒ x = 4, y = −2.

⎩

Therefore, the point T (4, −2, 0) lies on the line.

Therefore, the equation of the sought line has the form:

x − 4

−3

y + 2

z

\=

\=

.

(9.7)

1

−2





9.3 Angle Between Two Lines

323

**9.2 Equation of a Line That Passes Through the Two**

**Speciﬁed Points**

Assume that the line L passes through the points T (x , y , z ) and T (x , y , z ).

1

1

1

1

2

2

2

2

−−→

Then, the vector **a** = T T = (x −x , y −y , z −z ) is parallel to the line L, and

1

2

2

1

2

1

2

1

the **equation of a line that passes through the two speciﬁed points** in canonical

form looks as follows:

x − x1

y − y1

z − z1

\=

\=

.

(9.8)

x2 − x1

y2 − y1

z2 − z1

Example 9.3 The line that passes through two points with the coordinates

(11, 2, −6) and (13, 0, 7) is represented by the equation:

x − 11

y − 2

−2

z + 6

\=

\=

.

(9.9)

2

13

**9.3 Angle Between Two Lines**

Consider two lines

x − x1

k1

y − y1

z − z1

m1

\=

\=

\=

\=

,

.

(9.10)

(9.11)

l1

x − x2

k2

y − y2

l2

z − z2

m2

The **angle between two lines** ω will be equal to the angle formed by the directing

vectors **a** = (k , l , m ) and **a** = (k , l , m ):

1

1

1

1

2

2

2

2

(**a**1 · **a**2)

k1k2 + l1l2 + m1m2

ω = arccos

= arccos +

\+

.

(9.12)

|**a** ||**a** |

1

2

2 + 2 +

2

1

2 + 2 +

2

2

k

l

m

k

l

2

m

1

1

2

Example 9.4 Given are the lines:

x − 4

y + 5

z + 1

−1

\=

\=

\=

\=

,

(9.13)

(9.14)

6

3

x − 2

y + 6

z + 2

.

2

1

−1

Show that these lines are collinear and ﬁnd the angle between them.





324

9 Equation of a Line in a Space

**Solution** The necessary and sufﬁcient condition of collinearity of the lines is the

−−→

equality to zero of the scalar triple product (**a** , **a** , T T ), where **a** = (6, 3, −1),

1

2

1

2

1

**a** = (2, 1, −1) are the directing vectors of the lines, and the points T and T have

2

1

2

the coordinates T (4, −5, −1), T (2, −6, −2).

1

2

−−→

Compute (**a** , **a** , T T ):

1

2

1 2





6

2

3 −1

1 −1


−−→


(**a**1, **a**2, T1T2) =

` `= 0

.

(9.15)



−2 −1 −1

Therefore, the lines are collinear. The angle ω between them is determined from

the condition

6 · 2 + 3 · 1 + (−1) · (−1)

8

cos ω = -

\-

= √

.

(9.16)

62 + 32 + (−1)2 22 + 12 + (−1)2

69

As a result, we obtain the angle between the two lines

8

ω = arccos √

69

.

(9.17)

**9.4 Angle Between a Line and a Plane**

Assume that the line L and the plane π intersect at some point, and assume that the

vectors are given: **n** = (A, B, C) is the normal vector of plane π, and **a** = (k, l, m)

is the directing vector (see Fig. [9.1](#br333)).

**Fig. 9.1** The angle α

between a line and a plane

**a**

**n**

β

α

T

π

L





9.4 Angle Between a Line and a Plane

325

If the line and the plane form the angle α, and the vectors **n** and **a** for the angle

π

β, then α + β = . Then,

2

$

%

(**n** · **a**)

|**n**||**a**|

π

cos β =

, cos β = cos

− α = sin α,

(9.18)

2

and the **angle** α **between the line and the plane** is determined from the condition:

(**n** · **a**)

|**n**||**a**|

Ak + Bl + Cm

sin α =

= √

√

.

(9.19)

A + B + C k + l + m

2

2

2

2

2

2

**Condition of parallelism of the line** L **and the plane** π (including the belonging

of L and π):

Ak + Bl + Cm = 0.

(9.20)

**Condition of perpendicularity of the line** L **and the plane** π:

A

k

B

l

C

\=

\=

.

(9.21)

m

a

b

c

(Here, the equalities of the form

\=

are understood in terms of ad = bc.)

d

We obtain the condition of belonging of the line

x − x1

y − y1

z − z1

m

\=

\=

(9.22)

k

l

to the plane Ax + By + Cz + D = 0.

For this, it is necessary and sufﬁcient that the point T (x , y , z ) should lie on

1

1

1

1

the plane, and the vectors **n** = (A, B, C) and **a** = (k, l, m) should be perpendicular

to each other. Therefore, the **condition of the line’s belonging to the plane** consists

in the fulﬁlment of the equalities:

Ax1 + By1 + Cz1 + D = 0,

(9.23)

Ak + Bl + Cm = 0.





326

9 Equation of a Line in a Space

**9.5 Condition of Two Lines’ Belonging to a Plane**

The two lines:

x − x1

k1

y − y1

l1

z − z1

m1

L1 :

\=

\=

, passing through the point T1(x1, y1, z1), and

z − z2

, passing through the point T2(x2, y2, z2),

x − x2

k2

y − y2

\=

l2

L2 :

\=

m2

in space can

\1. intersect;

\2. be parallel;

\3. be skew.

In the ﬁrst two cases, they lie in the same plane. The two lines that do not intersect

and are not parallel are called **skew lines**.

The necessary and sufﬁcient **condition of belonging of the lines** L1 **and** L2

**to the same plane** consists in coplanarity of the vectors **a**1 = (k , l , m ), **a**

\=

1

1

1

2

−−→

(k2, l2, m2) and T1T2 = (x2 − x1, y2 − y1, z2 − z1), i.e. the determinant’s equality

to zero must be valid:




− x y − y z − z

x2

1

2

1

2

1



` `= 0

(9.24)

.

k1

l1

m1





k2

l2

m2

**Condition of parallelism of two lines**:

k1

k2

l1

l2

m1

m2

\=

\=

.

(9.25)

For **intersection of lines**, it is sufﬁcient that at least one of the equalities ([9.25](#br335))

is violated and the condition ([9.24](#br335)) is valid.

Example 9.5 Find the planes that pass through the line

x − 4

−8

y − 8

−1

z + 1

\=

\=

(9.26)

3

and are orthogonal to the plane −3x + y + z + 3 = 0.

**Solution** The directing vector of the given line **a** = (−8, −1, 3) is the normal

vector to the plane **n** = (−3, 1, 1).





9.5 Condition of Two Lines’ Belonging to a Plane

327

**Fig. 9.2** To Example [9.5](#br335).

Mutual arrangement of the

−−→

vectors **a** and T T

0

T0

T

**a**

The point T0(4, 8, −1) belongs to the sought plane since it lies on the line (see

Fig. [9.2](#br336)).

Write the equation of the plane that passes through the point T and is parallel to

−−→

the two vectors **a** and **n** (the vectors **a**, **n** and T T are coplanar):

0




− 4 y − 8 z + 1

x




` `= 0

(9.27)

(9.28)

−8 −1

3

,




` `−3

1

1 

hence:

− 4(x − 4) − (y − 8) − 11(z + 1) = 0.

Thus, we obtain the sought equation of the plane:

4x + y + 11z − 13 = 0.

(9.29)

Example 9.6 Find the equation of the plane that passes through the two parallel

lines:

x − U1

y − V1

z − W1 x − U2

y − V2

z − W2

\=

\=

,

\=

\=

,

(9.30)

k

l

m

k

l

m

and at least one of the inequalities is valid: U = U , V = V , W = W .

1

2

1

2

1

2

**Solution** The sought plane passes through the points T (U , V , W ) and

1

1

1

1

T2(U2, V2, W2) and is parallel to the directing vector **a** = (k, l, m). On the other

−−→

hand, this plane is parallel to the vector T T = (U − U , V − V , W − W ).

1

2

2

1

2

2

2

1





328

9

Equation of a Line in a Space

Let T (x, y, z) be the current point of the plane.

−−→

1

−−→

Write the condition of coplanarity of the vectors T T , **a** and T T :

1 2




− U1 y − V1 z − W

1 

` `x



` `= 0

(9.31)

.

k

l

m




−

−

−

U2 U1 V2 V1 W2 W1

The relation ([9.31](#br337)) sets up the equation of the plane that passes through two

parallel lines.

**Review Questions**

\1. Write the equation of a straight line that passes through a speciﬁed point parallel

to a speciﬁed vector.

\2. What does the equation of a line in space that passes through two speciﬁed points

look like?

\3. Write the formula for computing an angle between lines in space.

\4. How is an angle between a line and a plane computed?

\5. Formulate the condition of parallelism of a line and a plane.

\6. Write the condition of perpendicularity of a line and a plane.

\7. What lines are called skew lines?

\8. What is the condition of parallelism of two lines in space?

**Problems**

**9.1**. Find the intersection points of the line speciﬁed by the equation

2x + 4y + z + 9 = 0,

4x − 6y − 2z + 1 = 0,

with the coordinate planes.

**9.2**. Find the equation of the plane that passes through the two parallel lines:

x − 2

y

z − 1

−3

x

y + 1

z + 1

−6

\=

\=

,

\=

\=

.

2

3

4

6

**9.3**. Find the coordinates of the foot of the perpendicular dropped from the point

T (0, 2, −4) onto the plane x + y − z + 3 = 0.





Problems

329

x − 2

y

**9.4**. Determine whether the plane 8x − 3z + 11 = 0 and the line

z − 1

\=

\=

2

3

are parallel.

8

x − 1

**9.5**. Determine whether the plane x + 2y − z − 2 = 0 and the line

\=

3

y + 1

z

\=

are parallel?

3

−1

**9.6**. Write the necessary and sufﬁcient condition of perpendicularity of the plane

x − x0

y − y0

z − z0

Ax + By + Cz + D = 0 and the line

\=

\=

.

k

l

m

x − x0

y − y0

z − z0

m

**9.7**. Prove that the condition of belonging of the line

\=

\=

k

l

to the plane Ax + By + Cz + D = 0 has the form

Ax0 + By0 + Cz0 + D = 0,

(9.32)

Ak + Bl + Cm = 0.

x − x1

∗**9.8.** Show that the distance from the point T (x , y , z ) to the line

\=

0

0

0

0

k

y − y1

z − z1

\=

can be calculated by the formula

l

m

.

2

2

2

F + F + F

1

2

3

d =

,

2 + 2 +

l

m

2

k

where the following designations are introduced


















l

m

m

k

k

l

F1 =


, F2

\= 

, F3

\= 

.






y − y z − z 

z − z x − x 

x − x y − y 

1

0

1

0

1

0

1

0

1

0

1

0

x + 1

**9.9**. Find the acute angle between the lines speciﬁed by the equations

\=

2

y − 9

−5

z + 2

x

y + 1

−6

z + 4

\=

and

\=

\=

.

2

3

3

x + 1

−1

y − 9

−5

z + 2

**9.10**. Find the obtuse angle between the lines

\=

\=

and

7

x − 3

−3

y − 9

z

\=

\=

.

3

5

**9.11**. Find the equation of the plane that passes through the line

x − 10

−7

y

z + 10

−1

\=

\=

(9.33)

3





330

9

Equation of a Line in a Space

parallel to the line

x + 1

y + 2

z − 6

\=

\=

.

(9.34)

2

4

8

x − x1

k1

y − y1 z − z1

\=

l1 m1

∗**9.12.** Compute the distance between the skew lines

\=

x − x2

k2

y − y2

l2

z − z2

m2

and

\=

\=

.

**Answers and Solutions**

[**9.1**](#br337)[** ](#br337)Answer:

[$](#br337)

% $

% $

%

29

14

17

19

8

17

19

−

, − , 0 ,

−

, 0, − , , 0, − , 29 .

14

4

2

[**9.2**](#br337)[** ](#br337)Answer:

9x − 10y − 4z − 14 = 0.

[**9.3**](#br337)[** ](#br337)Solution.

Write the equation of the line that passes through the point T perpendicular to

the plane:

x

y − 2

z + 4

−1

\=

\=

.

(9.35)

1

1

Represent the equation of this line in parametric form:

x = u, y = u + 2, z = −u − 4,

(9.36)

where u ∈ R.

Substitute these coordinates into the equation of the plane:

u + (u + 2) − (−u − 4) + 3 = 0,

hence, we obtain u = −3.

(9.37)

Knowing u, ﬁnd the coordinates of the intersection point of the line and the plane:

x = −3, y = −1, z = −1.

(9.38)

So, the intersection point of the perpendicular dropped from the point T onto the

plane has the coordinates (−3, −1, −1).





Answers and Solutions

331

[**9.4**](#br338)[** ](#br338)Solution.

x − x0

y − y0

z − z0

m

The condition of parallelism of the line

\=

\=

and the

k

l

plane Ax+By+Cz+D = 0 reduces to fulﬁlment of the equality Ak+Bl+Cm = 0

that reﬂects orthogonality of the directing vector **τ** = (k, l, m) and the normal to

the plane **n** = (A, B, C).

According to the problem statement, **τ** = (2, 3, 8), **n** = (8, 0, −3).

Since the equality to zero of the scalar product (**τ** · **n**) = 0 is valid, then the line

and the plane are parallel.

x − 1

y + 1

z

[**9.5**](#br338)[** ](#br338)Answer: no, the plane x + 2y − z − 2 = 0 and the line

\=

\=

3

3

−1

are not parallel.

[**9.6**](#br338)[** ](#br338)Solution.

The normal vector of the plane Ax + By + Cz + D = 0 has the coordinates

x − x0

y − y0

(A, B, C). At the same time, the directing vector of the line

\=

\=

k

l

z − z0

is equal to (k, l, m).

m

In order for the line to be perpendicular to the plane, it is necessary and sufﬁcient

that the normal vector of the plane be collinear with the directing vector of the line:

A

k

B

l

C

\=

\=

.

m

[**9.7**](#br338)[** ](#br338)Proof.

Indeed, the ﬁrst equation ([9.32](#br338)) means that the point (x , y , z ), through which

0

0

0

the line passes, belongs to the plane. The second equation reﬂects the fact of

parallelism of the line and the plane (see Problem [**9.4**](#br338)).

[**9.8**](#br338)[** ](#br338)Proof.

From the equation of a line, we ﬁnd the coordinates of its directing vector **s** =

(l, m, n). Denote the point (x1, y1, z1) that lies on this line by T1(x1, y1, z1).

It is known from the properties of the vector product that the modulus of the

vector product of vectors is equal to the area of the parallelogram constructed on

these vectors:

−−→

S = |T0T1 × **s**|.

On the other hand, the area of the parallelogram is equal to the product of its side

by the height drawn to this side: S = |**s**|d.

In our case, the height of the parallelogram is equal to the distance d from the

point to the plane, and its side is equal to the modulus of the directing vector |**s**|.





332

9 Equation of a Line in a Space

Having equated the expressions for the area, it is easy to obtain a formula of the

distance from the point to the line:

−−→

|T T × **s**|

0

1

d =

.

|**s**|

Hence, we ﬁnd





**i**

**j**

**k**

−−→


T0T1 × **s** = x − x y − y z − z


` `1

0

1

0

1

0




k

l

m

= (m(y − y ) − l(z − z ))**i**

1

0

1

0

\+ (k(z − z ) − m(x − x ))**j**

1

0

1

0

\+ (l(x − x ) − k(y − y ))**k**.

1

0

1

0

Thus,

−−→

|T T × **s**|

0

1

4

5





2

2

2

5





5





l

m

m

k

k

l

= 6

` `+ 

` `+ 

` `,






y − y z − z 

z − z x − x 

x − x y − y 

1

0

1

0

1

0

1

0

1

0

1

0

where

\-

|**s**| = k2 + l2 + m2.

Therefore,

4

5





2

2

2

5





5

l

m


m

k


k

l

6

` `+ 

` `+ 







y − y z − z 

z − z x − x 

x − x y − y 

1

0

1

0

1

0

1

0

1

0

1

0

d =

√

.

2 + 2 +

l

m

2

k

[**9.9**](#br338)[** ](#br338)Solution.

The lines are speciﬁed in canonical form.

Find the angle α between their directing vectors **a** = (2, −5, 2) and **b** =

(3, −6, 3):

(**a** · **b**)

cos α =

;

|**a**| · |**b**|





Answers and Solutions

333

2 · 3 + (−5) · (−6) + 2 · 3

14

cos α = -

\-

\=

√

3 22

.

22 + (−5)2 + 22 · 32 + (−6)2 + 32


14

The sought angle is α = arccos

√

.

3 22

[**9.10**](#br338)[** ](#br338)Solution.

Find the angle α between the directing vectors **a** = (−1, −5, 7) and **b** =

(−3, 3, 5) of the speciﬁed lines:

**a** · **b**

cos α =

.

|**a**||**b**|

We substitute here the numeric values from the problem statement and obtain

(−1) · (−3) + (−5) · 3 + 7 · 5

23

cos α = -

\-

\=

√

5 129

.

(−1)

2 + −5 2 + 72 −3 2 + 32 + 52

(

)

(

)


23

Therefore, the sought angle is π − α = π − arccos

√

5 129

.

[**9.11**](#br338)[** ](#br338)Solution.

The sought plane is parallel to the directing vectors **a** = (−7, 3, −1) and **a** =

1

2

(2, 4, 8) and passes through the point T0(10, 0, −10) that lies on the ﬁrst line. Thus,

−−→

the vectors **a** , **a** and T T are coplanar.

1

2

0

−−→

Expanding the determinant that expresses the scalar triple product (T T , **a** , **a** ),

0

1

2

for example, in the ﬁrst row, we obtain




− 10 y z + 10

x




` `= 28 − 10 + 54 − 34 + 10 = 0

−7

3

−1

(x

)

y

(z

)

,





2

4

8

and we ﬁnally obtain

14x + 27y − 17z − 310 = 0.

[**9.12**](#br339)[** ](#br339)Solution.

Introduce the designations T (x , y , z ), T (x , y , z ), **a** = (k , l , m ), **a** =

1

1

1

1

2

2

2

2

1

1

1

1

2

(k2, l2, m2).

−−→

Consider the parallelogram constructed on the vectors T T , **a** and **a**2, and

1

2

1

compute its volume V .

On the one hand, the volume V is equal to the product of the module of the

vector product |**a** × **a** | and the height of the parallelogram. On the other hand,

1

2

−−→

V = abs(T1T2, **a**1, **a**2).





334

9 Equation of a Line in a Space

Since the sought distance d between the skew lines is equal to the height, then

−−→

abs(T T , **a** , **a** )

1

2

1

2

d =

,

or

|**a** × **a** |

1

2




− x y − y z − z

x2

1

2

1

2

1


abs 


k1

k2

2

l1

m1





l2

m2

d = 4

.

5





2

2

5





5k l 

l m 

m k 

1

1

1

1

1

1

6

` `+ 

` `+ 







k l 

l m 

m k 

2

2

2

2

2

2





**Chapter 10**

**Bilinear and Quadratic Forms**

**10.1 Bilinear Forms**

Assume that in a n-dimensional vector space L a basis B = (**e** , **e** , . . . , **e** ) is

n

1

2

n

speciﬁed. Consider two vectors belonging to the space L :

n

n

i=1

n

i=1

**x** =

x **e** , **y** =

y **e** ,

i i

(10.1)

i

i

where x , y ∈ R for all i = 1, 2, . . . , n.

i

i

The linear combination of all possible products of the projection of the vectors **x**

and **y** on the basic normalized vectors

n

a x y ,

ij i j

(10.2)

i,j=1

where aij are arbitrary real numbers, is referred to as the **bilinear form** of A(**x**, **y**)

deﬁned on the basis B. The matrix A = (a ), where 1  i, j  n, is called the

ij

**matrix of bilinear form**. As is easy to see, an arbitrary bilinear form can be written

with the help of the matrix multiplication operation as

A(**x**, **y**) = **x**TA **y**.

(10.3)

The following **properties of linearity** of the form are fulﬁlled for each of its

arguments:

∀**x**, **y**, **z** ∈ Ln and ∀α ∈ R

\1. A(**x** + **y**, **z**) = A(**x**, **z**) + A(**y**, **z**),

\2. A(α**x**, **z**) = αA(**x**, **z**),

© Springer Nature Switzerland AG 2021

335

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_10>





336

10 Bilinear and Quadratic Forms

\3. A(**x**, **y** + **z**) = A(**x**, **y**) + A(**x**, **z**),

\4. A(**x**, α**z**) = αA(**x**, **z**).

A bilinear form is referred to as **symmetric**, if for any **x**, **y** ∈ L the condition

n

A(**x**, **y**) = A(**y**, **x**) is fulﬁlled.

A bilinear form is referred to as **positively deﬁnite**, if ∀**x** ∈ L , **x** = **0**, the

n

inequality A(**x**, **x**) > 0 is fulﬁlled.

Example 10.1 Consider the vectors **x** = (x , x , x ) and **y** = (y , y , y ) of some

1

2

3

1

2

3

three-dimensional vector space, and the bilinear form A(**x**, **y**) = x y + 3x y +

1

1

2 2

8x y , deﬁned on the basis of this space. The matrix A of bilinear form will in this

3

3

case have the following diagonal form:

⎡

⎤

1 0 0

⎢

⎥

A = 0 3 0

⎢

⎥

.

(10.4)

⎣

⎦

0 0 8

Represent A in matrix notation:

⎡

⎤ ⎡

⎤

1 0 0

0 3 0

0 0 8

y1

y2

y3

⎢

⎥ ⎢

⎥

A(**x**, **y**) = **x**T A **y**

= [

x , x , x

1 3

] ⎢

⎥ ⎢

⎥

2

⎣

⎦ ⎣

⎦

⎡

⎤

y1

⎢

⎥

= [x , 3x , 8x ] ⎢ ⎥ = x y + 3x y + 8x y .

(10.5)

1

2

3

y2

1

1

2

2

3 3

⎣

⎦

y3

It is easy to show that it has the properties of symmetry and positive deﬁniteness:

A(**x**, **y**) = x y + 3x y + 8x y = y x + 3y x + 8y x

1

1

2

2

3

3

1

1

2

2

3 3

= A(**y**, **x**) ⇒ the form is symmetric;

(10.6)

(10.7)

2

2

2 

3

A(**x**, **x**) = x + 3x + 8x

0 for all non-zero vectors **x**

1

2

⇒ A(**x**, **y**)is a positively deﬁnite form.

Example 10.2 M(**x**, **y**) = x y − x y − x y − x y is a bilinear form on R

\4. As

1

1

2

2

3

3

4 4

is easy to see, it is symmetric, but not positively deﬁnite. [Not](#br421)e that this form deﬁnes

the space-time metric in the special theory of relativity [[45](#br421)[\].](#br421)






10.2 Quadratic Forms

337

**10.2 Quadratic Forms**

**Quadratic form** will be referred to as the expression

ω(**x**) = A(**x**, **x**),

(10.8)

where A(**x**, **x**) is some bilinear form. The name “quadratic form” is associated with

the fulﬁlment for this expression of the property of the second degree homogeneity

in the argument of the form: ∀α ∈ R the following equation is valid:

ω(α**x**) = α2ω(**x**).

(10.9)

Example 10.3 In the basis of the bilinear form M(**x**, **y**), deﬁned in Example [10.2](#br345)

on page [336](#br345), we can construct the quadratic form

2

2

2

2

4

μ(**x**) = M(**x**, **x**) = x − x − x − x

(10.10)

1

2

3

that depends on four variables: x , x , x and x .

1

2

3

4

If in the n-dimensional vector space Ln the basis is speciﬁed and the vector

**x** = [x , x , . . . , x ]

T is selected, then

1

2

n

n

ω(**x**) = **x**T A **x**

\=

(10.11)

a x x ,

ij i j

i,j=1

which allows interpreting the quadratic form as a function speciﬁed on the set of all

possible vectors **x**.

The matrix A = (a ) is referred to as the **matrix of quadratic form** ω(**x**). This

ij

matrix can be deemed symmetric, since the expression of the form a x x +a x x ,

ij

i

j

ji j i

due to commutativity of multiplication of real numbers, can always be represented

as

a x x + a x x ≡ 1a x x +1a x x ,

(10.12)

ij

i

j

ji

j

i

ij

i

j

ji j i

where the designation 1a = 1a = (a + a )/2 is introduced.

ij

ji

ij

ji

So, an arbitrary quadratic form in some basis can be speciﬁed in matrix form:

**x**T A **x**,

(10.13)

where **x** = (x , x , . . . , x ) is the column composed of variables, and the matrix

1

2

n

A of quadratic form always allows a notation in symmetric form: a = a for all

ji

ij

i, j = 1, . . . , n.





338

10 Bilinear and Quadratic Forms

The symmetric bilinear form A(**x**, **y**) is referred to as **polar** to the quadratic form

ω(**x**) = A(**x**, **x**). For the quadratic form, the formula is valid:

17

8

A(**x**, **y**) = ω(**x** + **y**) − ω(**x**) − ω(**y**) .

(10.14)

2

Example 10.4 Find the bilinear form polar to ω(**x**) = x x + x x + x x .

1

2

2

3

1 3

**Solution** According to the deﬁnition of polar form ([10.14](#br347)), we obtain

17

A(**x**, **y**) = (x + y )(x + y ) + (x + y )(x + y ) + (x + y )(x + y )

1

1

2

2

2

2

3

3

1

1

3

3

2

8

− (x x + x x + x x ) − (y y + y y + y y ) .

(10.15)

1

2

2

3

1

3

1

2

2

3

1 3

After algebraic transformations, we ﬁnd the expression for the sought bilinear form:

1

A(**x**, **y**) = (x y + x y + x y + x y + x y + x y ).

(10.16)

1

2

1

3

2

1

2

3

3

1

3 2

2

When passing to a new basis, i.e. during nondegenerate change of the variables

x1, x2, ..., xn with the change matrix C, the matrix A of quadratic form in the new

basis will take the form:

T

A = C A C.

(10.17)

It is known that changing the basis does not result in the change of the rank of

the matrix in quadratic form.

Rank of the matrix in quadratic form is referred to as the **rank of quadratic**

**form**. If this matrix has a rank equal to the dimension of the vector space, i.e. the

number of variables n, then the quadratic form is called **nondegenerate**, and if the

rank is less than n, then it is called **degenerate**.

Example 10.5 Find the matrix of quadratic form of the three variables:

2

2

2

ω(**x**) = 3x + 2x1x2 − 5x1x3 − x + x .

(10.18)

1

2

3

**Solution** The diagonal elements aii of the matrix of quadratic form ω(**x**) are

deﬁned as the coefﬁcients of the quadratic summands x2, and the non-diagonal ones

i

a , where i = j, are twice smaller than the respective coefﬁcients of the summands

ij

of the form x x :

i

j

⎡

⎤

3

1 −5/2

⎢

⎥

A =

⎢

1

−1

0

⎥

.

(10.19)

⎣

⎦

−5/2 0

1





10.3 Bringing the Quadratic Form to the Canonical Form

339

Using any of the known methods for computing the rank of the matrix, for

example, the method of bringing to echelon form, we ﬁnd rk A = 3. Since the

tank of the matrix A is equal to the number of variables, then this quadratic form is

nondegenerate.

In matrix notation, the quadratic form can be represented in the form:

⎡

⎤ ⎡

⎤

3

1 −5/2

x1

x

⎢

⎥ ⎢

⎥

ω(**x**) = [x1, x2, x3]

⎢

1

−1

0

⎥ ⎢

⎥

.

(10.20)

⎣

⎦ ⎣ 2⎦

−5/2 0

1

x

3

**10.3 Bringing the Quadratic Form to the Canonical Form**

If, in some basis, the matrix of quadratic form takes diagonal form

⎡

⎤

λ1 0 0 . . .

0

0

0

0

⎢

⎥

⎢

⎥

0 λ2 0 . . .

⎢

⎥

⎢

⎥

` `= . . . . . . . . . . . . . . . . . . . .

⎢

⎥

,

(10.21)

⎢

⎥

⎢

⎥

⎢ 0 0 0

0 ⎥

. . . λn−1

⎣

⎦

0 0 0 . . .

0

λ

n

then, as is easy to see, the quadratic form is formed by a linear combination of

squares of the variables x , x , ..., x :

1

2

n

2

2

2

ω(**x**) = λ1x + λ2x + · · · + λ x .

(10.22)

1

2

n

n

The crossing summands of the form x x for i = j are in this case not included into

i

j

the expression for ω(**x**).

Among the coefﬁcients λ , where i = 1, 2, . . ., n, there can be positive numbers,

i

negative numbers and numbers equal to zero.

**Theorem 10.1** For each quadratic form, there exists a basis, in which it has the

**canonical form**:

n

2

i

ω(**x**) =

λ x .

i

(10.23)

i=1

Attention should be paid to the fact that the canonical basis is deﬁned non-

uniquely.





340

10 Bilinear and Quadratic Forms

**10.3.1 Lagrange’s Method of Separating Perfect Squares**

In applications, we often come across a problem of bringing a quadratic form to a

diagonal form. Several methods have been suggested for solving this problem.

**Lagrange’s method** of bringing the quadratic form to the canonical form

consists in the following.

n

Assume that the quadratic form ω(**x**) =

basis of the space Ln.

a x x is given, deﬁned in the

ij i j

i,j=1

2

Depending on the presence in the sum of the summands of the form a x ,

ii

i

consider two cases.

\1. At least one of the coefﬁcients att of the quadratic summands is not equal to zero.

The main idea of the method consists in separating the perfect square, uniting all

the summands that contain the variable xt . The obtained perfect square is used as the

basis for change of the variables, excluding the terms linear in xt . If in the form still

remain crossing variables of the form x x , then we return to the beginning of the

i

j

procedure. Otherwise, the form contains only quadratic summands, and the solution

is complete.

As we can see, without loss of generality, we may assume that a11 = 0.

Consider the ﬁrst step of Lagrange’s method in more detail.

Denote by S the sum of all summands containing x1:

2

S = a11x + 2a12x1x2 + · · · + 2a1 x1x ,

(10.24)

(10.25)

1

n

n

and complete the square of S. We obtain

$

%

2

a12

a11

a1n

a11

S = a11 x1 +

x2 + · · · +

xn − R,

where the expression R does not contain x1 in its notation.

Then, change the variables

⎧

a12

a11

a1n

⎨  =

\+

\+ · · · +

a11

x

x1

x2

x ,

n

1

(10.26)

(10.27)

⎩

i

x = x for i = 2, . . ., n.

i

Then, the quadratic form in the new basis will take the form:

n

2



ij i j

ω(**x**) = a11(x ) +

a x x .

1

i,j=2





10.3 Bringing the Quadratic Form to the Canonical Form

341

From here on, the same method can be applied to the variables x , x and so on,

2

3

to ﬁnally exclude all summands of the form x x for i = j.

i

j

\2. All coefﬁcients are aii = 0.

In this case, select aij = 0 for some i = j and change the variables:

⎧

⎪

\=

` `+

x ,

j

⎪x

x

⎨ i

i


(10.28)

x = x − x ,

j

⎪

i

k

j

⎪

⎩

x = x for k = i, j.

k

As a result, each product x x will be presented in the form of a linear

i

j

combination of the quadratic summands x x = (x)2 − (x )2, and we will arrive at

i

j

i

j

the ﬁrst case.

After step (1) and, when necessary, step (2), bringing of the quadratic form to the

diagonal form will be completed.

Example 10.6 Using Lagrange’s method, bring the following form to the canonical

one

2

2

ω(**x**) = 2x1x2 − 6x1x3 − x + 5x .

(10.29)

2

3

**Solution** Collect the summands that contain x2:

2

2

2

2

2

2

−x + 2x x −6x x + 5x = − (x − 2x x + x ) + x − 6x x + 5x

2

1

2

1

3

3

2

1

2

1

1

1

3

3



!



!   !

S

perfect square

−R

2

2

1

2

3

= −(x − x ) + x − 6x x + 5x .

(10.30)

1

2

1

3

Change the variables:

⎧

⎪

⎪y = x ,

⎨ 1

1

y2 = x1 − x2,

y3 = x3.

(10.31)

(10.32)

⎪

⎪

⎩

As a result, we obtain the form

2

2

1

2

3

ω(**y**) = −y + y − 6y1y3 + 5y .

2

Now collect the summands that contain y1, and complete the square of them

2

2

2

2

2

3

ω(**y**) = −y + (y − 6y1y3 + 9y ) − 9y + 5y

2

1

3

3

2

2

2

3

= −y + (y − 3y ) − 4y .

(10.33)

2

1

3





342

10 Bilinear and Quadratic Forms

Perform the second change of the variables:

⎧

⎪

\=

− 3

⎪z

y1

3

y ,

⎨ 1

z2 = y2,

z3 = y3.

(10.34)

⎪

⎪

⎩

We ﬁnally obtain ω(**z**) = z2 − z2 − 4z2.

1

2

3

Example 10.7 Using Lagrange’s method, bring the following form to the canonical

one

ω(**x**) = x1x2 + x1x3 + x2x3.

(10.35)

**Solution** Since there are no summands of the form x2 in this expression, we change

i

the variables

⎧

⎪



2

⎪x = x + x ,

⎨ 1

1

2

(10.36)

x2 = x − x ,

⎪

1

⎪

⎩

x3 = x ,

3

as a result of which we obtain


ω(**x**) = (x ) + 2x x + (x ) − (x ) − (x )

2



2

2

2

(10.37)

(10.38)

1

1

3

3

2

3


3

2

2

2

2

= (x + x ) − (x ) − (x ) .

1

3

The new change

⎧

⎪

\=

` `+

x ,

3

⎪y

x

⎨ 1

1

y2 = x ,

(10.39)

⎪

2

3

⎪

⎩

y3 = x

results in the form

2

2

2

ω(**y**) = y − y − y ,

(10.40)

1

2

3

1

1

where y1 = (x + x ) + x , y = (x − x ), y = x .

1

2

3

2

1

2

3

3

2

2





10.3 Bringing the Quadratic Form to the Canonical Form

343

**10.3.2 Jacobi Method**

Let the following determinants composed of the elements of the matrix A = (a )

ij

of the quadratic form ω(**x**) be other than zero:






a11 a12

1 = a11, 2 =


,

. . . ,

(10.41)


a a 

21 22




a11 a12 . . . a1 

n




a21 a22 . . . a2

n

` `= 

(10.42)

` `.

n

.

.

.

.

.

` `.

.

.

. 

` `.

.

.





a 1 a 2 . . . a

n

n

nn

Then, there exists the basis B = (**e** , **e** , . . . , **e** ), in which ω(**x**) is presented in the

1

2

n

form:

1

0

2

1

n

2

2

2

n

ω(**z**) =

z +

z + · · · +

z ,

(10.43)

1

2

n−1

where z , i = 1, 2, . . . , n, denote the coordinates of the vector **x** in the new basis

i

B, and for uniformity, we assume that 0 = 1. This is the essence of the **Jacobi**

**method** of bringing the quadratic form to the canonical form.

In comparison with Lagrange’s method, the Jacobi method has an advantage that

the transition to the basis B is direct, without any intermediate steps.

The transition from the basis (**e** , **e** , . . . , **e** ) to the canonical basis

1

2

n

(**c**1, **c**2, . . . , **c**n) is performed by the formulae

i

**c**i =

η **e** , i = 1, 2, . . . , n,

(10.44)

(10.45)

ij

j

j=1

i−1,j

ηij = (−1)i+j

,

i−1

where 

is the minor of the matrix formed by the elements from (aij ) that

i−1,j

are situated at the intersection of the rows numbered k = 1, 2, . . ., i − 1 with the

columns numbered k = 1, 2, . . . , j − 1, j + 1, . . . , i.

Note that the introduced determinants  ,  , ...,  are called the **corner**

1

2

n

**minors** of the matrix of quadratic form.

**Rank** of quadratic form is the number of non-zero coefﬁcients λi = 0.





344

10 Bilinear and Quadratic Forms

Let us introduce the following designations:

• n —number of positive coefﬁcients of λ > 0,

\+

i

• n —number of negative coefﬁcients of λ < 0,

−

i

• n —number of coefﬁcients equal to zero of λ = 0.

0

i

The ordered set of integral non-negative numbers (n , n , n ) is called the

\+

−

0

**signature** of quadratic form.

The quadratic form ω(**x**) is referred to as **positively deﬁnite**, if for any non-zero

**x** the inequality

ω(**x**) > 0

(10.46)

is fulﬁlled, and **negatively deﬁnite**, if ω(**x**) < 0 is fulﬁlled.

The quadratic form ω(**x**) is referred to as **alternating**, if there exist such **x**1 and

**x**2, that the following inequalities occur

ω(**x**1) > 0, ω(**x**2) < 0.

(10.47)

**Sylvester’[s**](#br353)[**1](#br353)[ ](#br353)Criterion** For the positive deﬁniteness of the quadratic form ω(**x**),

it is necessary and sufﬁcient that all the primary minors of its matrix should be

positive:  > 0,  > 0, ...,  > 0.

1

2

n

For the negative deﬁniteness of the quadratic form ω(**x**), it is necessary and

sufﬁcient that the signs of the corner minors of its matrix should alternate, and

1 < 0.

**The Law of Inertia** The number of summands with positive (negative) coefﬁcients

of a quadratic form brought to the canonical form does not depend on the method

used to obtain such a representation.

**Review Questions**

\1. Deﬁne bilinear form.

\2. Enumerate the property of linearity of bilinear forms.

\3. What bilinear forms are called symmetric and positively deﬁned?

\4. Deﬁne quadratic form.

\5. Explain why a matrix of an arbitrary quadratic form can always be deemed to

be symmetric.

\6. What bilinear form is called polar to the quadratic form?

\7. How is the rank of a quadratic form determined?

\8. What is the difference between degenerate and nondegenerate quadratic forms?

1James Joseph Sylvester (1814–1897), English mathematician.





Problems

345

\9. Explain the methods of bringing quadratic forms to diagonal form: Lagrange’s

method and the Jacobi method.

\10. How are the corner minors of a matrix of quadratic form determined?

\11. Formulate Sylvester’s criterion.

\12. What is the law of inertia of quadratic forms?

**Problems**

**10.1**. Which of the following functions F(**x**, **y**) of the vectors **x** = (x , x ) ∈ R2

1

2

and **y** = (y , y ) ∈ R are bilinear forms?

2

1

2

(1) F(**x**, **y**) = x y + x y ;

√1

1

2 2

(2) F(**x**, **y**) = 2;

(3) F(**x**, **y**) = (x − y )2 − (x − y )2;

1

1

2

2

(4) F(**x**, **y**) = 4x y .

2

2

**10.2**. Find the bilinear form that is polar to the form:

2

2

3

(1) x − 2x x + 3x x + 7x ;

1

2

1 3

1

(2) −2x2 + 3x x + x x ;

1

3

2 3

1

(3) 3x x + x2;

1

3

2

2

1

2

2

2

3

(4) x + 4x x + 4x x − 4x − 2x x − x .

1

2

1

3

2 3

**10.3**. Bring to the canonical form the quadratic form of three variables:

2

2

3

(1) x + 2x x + 4x x − 4x ;

1

2

1 3

1

(2) x x + x x − 6x x ;

1

2

1

3

2 3

2

1

(3) −2x − 7x x ;

1

3

(4) x2 − 4x x + 12x x − x2 + 4x x + 3x2.

1

2

1

3

2 3

1

2

3

**10.4**. Bring to the canonical form the quadratic form of four variables:

2

2

2

2

(1) x + 2x x + 2x x + 2x x + 3x + 6x x + 8x x + x + 2x x + x ;

1

2

1

3

1

4

2

3

2

2

4

3 4

1

2

3

4

(2) x x + x x + x x + x x ;

1

2

1

4

2

3

3 4

2

1

2

2

2

4

(3) −5x + 2x x + 3x + x x − 2x x − x + 2x x + x ;

1

4

2

3

2

4

3 4

3

(4) x2 + x x + x x + x x + x2 + x x + x x + x2 + x x + x2.

1

2

1

3

1

4

2

3

2

4

3 4

1

2

3

4

**10.5**. Which of the following quadratic forms are positively deﬁnite, negatively

deﬁnite and alternating?

2

2

2

(1) x + x x + x ;

1

2

1

2

2

(2) x − 9x x + x ;

1

2

1

2

(3) x x + 2x x + 3x x + 4x x ;

1

2

1

4

2

3

3 4

(4) x x + x x .

1

2

3 4





346

10 Bilinear and Quadratic Forms

∗**10.6.** At what values of the real parameter a is the quadratic form:

2

2

2

ω(**x**) = ax + 2x1x2 + (10 − a)x

(10.48)

1

positively deﬁnite and negatively deﬁnite?

n

xixj

i + j − 1

∗**10.7.** Show that the form

is positively deﬁnite.

i,j=1

**Answers and Solutions**

[**10.1**](#br354)[** ](#br354)Answer:

The functions from items (1) and (4) are bilinear forms.

[**10.2**](#br354)[** ](#br354)Solution.

Use the formula ([10.14](#br347)) for the polar form:

(1)

17

8

A(**x**, **y**) = ω(**x** + **y**) − ω(**x**) − ω(**y**)

2

17

2

\=

(x + y ) − 2(x + y )(x + y )

1

1

1

1

2

2

2

2

\+ 3(x + y )(x + y ) + 7(x + y )

1

1

3

3

3

2

3

8

2

1

2

1

2

3

− (x − 2x x + 3x x + 7x ) − (y − 2y y + 3y y + 7y )

1

2

1

3

3

1

2

1

3

3

3

= x y − x y + x y − x y + x y + 7x y ;

1

1

1

2

1

3

2

1

3

1

3 3

2

2

(2)

17

2

A(**x**, **y**) =

− 2(x + y ) + 3(x + y )(x + y ) + (x + y )(x + y )

1

1

1

1

3

3

2

2

3

3

2

8

2

1

2

1

− (−2x + 3x x + x x ) − (−2y + 3y y + y y )

1

3

2

3

1

3

2 3

3

1

3

1

= −2x y + x y + x y + x y + x y ;

1

1

1

3

2

3

3

1

3 2

2

2

2

2

(3)

17

2

A(**x**, **y**) = 3(x + y )(x + y ) + (x + y )

1

1

3

3

2

2

2

8

2

2

− (3x x + x ) − (3y y + y )

1

3

2

1

3

2

3

3

\=

x y + x y + x y ;

2

1

3

2

2

3 1

2





Answers and Solutions

347

(4)

17

A(**x**, **y**) = (x + y )(x + y ) + 4(x + y )(x + y )

1

1

1

1

1

1

2

2

2

\+ 4(x + y )(x + y )

1

1

3

3

2

− 4(x + y ) − 2(x + y )(x + y ) − (x + y )(x + y )

− (x + 4x x + 4x x − 4x − 2x x − x )

− (y + 4y y + 4y y − 4y − 2y y − y )

2

2

2

2

3

3

3

3

3

3

2

1

2

2

2

3

1

2

1

3

2

3

8

2

1

2

2

2

3

1

2

1

3

2

3

= x y + 2x y + 2x y + 2x y − x y − 4x y

1

1

1

2

1

3

2

1

2

3

2

2

\+ 2x y − x y − x y .

3

1

3

2

3 3

[**10.3**](#br354)[** ](#br354)Solution.

(1) Transform the expression:

2

1

2

3

x + 2x1x2 + 4x1x3 − 4x

2

2

2

2

3

= x + 2x (x + 2x ) + (x + 2x ) − (x + 2x ) − 4x

= (x + x + 2x ) − (x + 2x ) − (2x ) .

1

1

2

3

2

3

2

3

2

2

2

1

2

3

2

3

3

Change the variables:

⎧

⎪

⎪y = x + x + 2x ,

⎨ 1

1

2

3

y2 = x2 + 2x3,

y3 = 2x3.

⎪

⎪

⎩

We obtain the quadratic form in the canonical form:

2

2

2

y − y − y .

1

2

3

(2) Change the variables:

⎧

⎪

\=

` `+

x ,

2

x ,

2

⎪x

x

⎨ 1

1

` `−

x2 = x

⎪

1

⎪

⎩

x3 = x .

3





348

10 Bilinear and Quadratic Forms

Transform the expression:

x1x2 + x1x3 − 6x2x3










= (x + x )(x − x ) + (x + x )x − 6(x − x )x

1

2

1

2

1

2

3

1

2

3

2

2

1







3

= (x ) − (x ) + x x + x x − 6x x + 6x x

1

2

3

2

3

1

3

2

2

2

2

1


2

= (x ) − (x ) − 5x x + 7x x

1

3

3




2

2

5

2

5

2




3

2

3

2

= (x ) − 5x x +

x

−

x

\+ 7x x − (x )

1

1

3

3

2

2








2

2

5

2

5

2




3

2

2

\=

\=

\=

x −

x

x

x

\+ 7x x − (x ) −

x

1

3

2

3






2

2

2

2

2

5

2

7

2

5

2

7

2


3



3

3

x −

−

−

x −

x

x

−

x

−

x

1

2

3


2

5

2

7

2


3



3

2

x −

x −

\+ 6(x ) .

1

2

3

Change the variables:

⎧

5

1

⎪


⎪y = x − x = (x + x − 5x ),

⎪ 1

1

2

3

1

3

⎨

2

2

7

1

y2 = x

` `−

x

` `=

(x1 x2

− 7x3),

−

⎪

2

3

⎪

2

2

⎪

√

⎩

y3 = 6x .

3

We obtain the quadratic form in the canonical form:

2

2

2

y − y + y .

1

2

3

(3) Transform the expression:

2

− 2x − 7x x

1

1 3

2 √

3

3

2 √

3

2

2

$√

%

2

7 2

7 2

= −

2x1 − 7x x −

x3

x3

\+

x3

1

3

4

4

2

√

3

2 √

2

2

√

7 2

4

7 2

\=

2x1 +

x3

\+

.

4





Answers and Solutions

349

Change the variables:

⎧

√

⎪

√

7 2

4

⎪

⎨

\=

\=

2

\+

y1

y2

x1

x3,

√

⎪

7 2

4

⎪

⎩

x3.

We obtain the quadratic form in the canonical form:

2

2

−y + y .

1

2

(4) Transform the expression:

2

2

2

3

x − 4x1x2 + 12x1x3 − x + 4x2x3 + 3x

1

2

2

2

= x − 4x (x − 3x ) + (2x − 6x )

1

1

2

3

2

3

2

2

2

3

− (2x − 6x ) − x + 4x x + 3x

2

3

2

2

3

2

2

2

2

2

2

2

3

= (x − 2x + 6x ) − 4x + 24x x − 36x − x + 4x x + 3x

= (x − 2x + 6x ) − 5x + 28x x − 33x

1

2

3

2

3

3

2 3

2

2

2

2

3

1

2

3

2 3

$√

%

2

2

= (x − 2x + 6x ) −

5x2 + 28x2x3

1

2

3

2

√

3

2

√

3

2

2

14 5

5

14 5

−

x3

\+

x3 − 33x2

3

5

2

√

3

2

√

14 5

5

31

5

2

2

= (x − 2x + 6x ) −

5x2 −

x3

\+

x .

3

1

2

3

Change the variables:

⎧

⎪y = x − 2x + 6x ,

⎪ 1

1

2

3

⎪


⎪

√

⎨

14

y2 = 5 x2 −

x3

,

5

⎪

,

⎪

⎪

31

⎪

⎩

y3 =

x3.

5

We obtain the quadratic form in the canonical form:

2

2

2

y − y + y .

1

2

3





350

10 Bilinear and Quadratic Forms

[**10.4**](#br354)[** ](#br354)Solution.

(1) Transform the expression:

2

2

2

2

4

x + 2x1x2 + 2x1x3 + 2x1x4 + 3x + 6x2x3 + 8x2x4 + x + 2x3x4 + x

1

2

3

2

2

2

= x + 2x (x + x + x ) + (x + x + x ) − (x + x + x )

1

1

2

3

4

2

3

4

2

3

4

2

2

2

2

4

\+ 3x + 6x x + 8x x + x + 2x x + x

2

3

2

2

4

3

3 4

2

2

2

3

2

4

= (x + x + x + x ) − x − 2x x − 2x x − x − 2x x − x

1

2

3

4

2

3

2

4

3 4

2

2

2

2

\+ 3x + 6x x + 8x x + x + 2x x + x

2

3

2

2

4

3

3 4

4

2

2

= (x + x + x + x ) + 2x + 4x x + 6x x

1

2

3

4

2

3

2 4

$√

%

2

2

= (x + x + x + x ) +

2x2 + 2x (2x + 3x )

1

2

3

4

2

3

4

1

2

1

2

2

\+

(2x + 3x ) − (2x + 3x )

3

4

3

4

2

2

√

3

2

√

√

3 2

2

2

= (x + x + x + x ) +

2x2 + 2x3 +

x4

1

2

3

4

2

√

3

2

√

3 2

2

−

2x3 +

x4

.

Change the variables:

⎧

⎪

\=

\+

\+

\+

⎪y1

x1 x2 x3 x4,

⎪

√

⎪

⎨

√

√

√

3 2

2

y2 = 2x2 + 2x3 +

x4,

⎪

⎪

⎪

√

3 2

2

⎪

⎩

y3 = 2x3 +

x4.

We obtain the quadratic form in the canonical form:

2

2

2

y + y − y .

1

2

3

(2) Change the variables:

⎧

` `+

⎪

\=

⎪x1

x

x ,

⎪

1

2

⎪

⎨

x2 = x − x ,

1

2

⎪

\=

` `+

⎪x

x

x ,

⎪ 3

3

4

⎪

⎩


4

x4 = x − x .

3





Answers and Solutions

351

Transform the expression:

x1x2 + x1x4 + x2x3 + x3x4





1


3

4

= (x + x )(x − x ) + (x + x )(x − x )

1

2

1

2

2





3

4


4

\+ (x − x )(x + x ) + (x + x )(x − x )

1

2

3

4

3

2

2

1




2

2

2

= (x ) − (x ) + 2x x − 2x x + (x ) − (x )

1

2

3

2

2

4

3

4

1

2

1

3

3

2

2

2

4

4

= (x ) + 2x x + (x ) − (x ) − 2x x − (x )

1

3

2

2

4

2

= (x + x ) − (x + x ) .

Change the variables:

⎧

1

2

⎪

⎪

\=

\=

` `+  =

\+

\+

\+

⎪y1

x

x

x

3

(x1 x2 x3 x4),

⎨

1

⎪

⎪

1

2

⎪

⎩

` `+  =

−

\+

−

y2

x

(x1 x2 x3 x4).

2

4

We obtain the quadratic form in the canonical form:

2

2

y − y .

1

2

(3) Transform the expression:

2

2

2

2

4

− 5x + 2x x + 3x + x x − 2x x − x + 2x x + x

1

1

4

2

2

3

2

4

3

3 4

2

2

= x + 2x (x − x + x ) + (x − x + x )

− (x − x + x ) − 5x + 3x + x x − x

= (x − x + x + x ) − 6x + 2x x + 2x − 2x x + 3x x − 2x

4

4

1

2

3

1

2

3

2

2

1

2

2

2

3

1

2

3

2

3

2

2

1

2

2

2

3

1

2

3

4

1

2

1

3

2 3

2√

3

2

$√

%

2

6

2

= (x − x + x + x ) −

6x1 + 2x (x − x ) −

(x − x )

1

2

3

4

1

2

3

2

3

6

2√

3

2

6

2

2

2

3

\+

(x − x ) + 2x + 3x x − 2x

2

3

2

3

6

2

√

6

3

2

√

2

= (x − x + x + x ) −

6x1 −

(x − x )

6

1

2

3

4

2

3

13

8

11

6

2

2

3

\+

x + x x −

x

2

2 3

6

3





352

10 Bilinear and Quadratic Forms

2

√

3

2

√

6

2

= (x − x + x + x ) −

6x1 −

(x − x )

1

2

3

4

2

3

6

2,

3

2 √

3

2 √

3

2

2

2

13

6

8

3

8 78

78

8 78

78

11

6

2

3

\+

x2

\+

x x +

x3

−

x3

−

x

2

3

2

√

3

2

√

6

2

= (x − x + x + x ) −

6x1 −

(x − x )

1

2

3

4

2

3

6

2,

√

3

2,

3

2

2

13

6

8 78

78

69

26

\+

x2 +

x3

−

x3

.

Change the variables:

⎧

⎪y = x − x + x + x ,

⎪ 1

1

√

2 √ 3

4

⎪

⎪

⎪

6

⎪

⎪

⎪y = 6x −

(x − x ),

⎨ 2

1

2

3

6 √

,

13

8 78

78

⎪

\=

\+

⎪y

x2

3

x ,

⎪ 3

⎪

6

69

⎪

,

⎪

⎪

⎪

⎩

y4 =

x3.

26

We obtain the quadratic form in the canonical form:

2

2

2

2

y − y + y − y .

1

2

3

4

(4) Transform the expression:

2

2

2

2

x + x1x2 + x1x3 + x1x4 + x + x2x3 + x2x4 + x + x3x4 + x

1

2

3

4

1

1

2

2

2

= x + x (x + x + x ) + (x + x + x ) − (x + x + x )

1

1

2

3

4

2

3

4

2

3

4

2

2

2

2

2

4

\+ x + x x + x x + x + x x + x

2

2

3

2

4

3

3

4


2

1

3

4

1

1

2

\=

\=

x1 + (x + x + x )

\+

\+

x + x x + x x

2

3

4

2

2

3

2 4

2

2

2

3

4

1

3

4

2

3

2

\+

x + x x +

x

4

3

4

2

2√

3


2

2

1

3

x1 + (x + x + x )

x2

2

3

4

2

2





Answers and Solutions

353

2√

3

2

1

3

\+

x (x + x ) +

(x + x )

2

3

4

3

4

2

6

2√

√

3

3

3


2

2

1

3

\=

\=

x1 + (x + x + x )

\+

x2 +

(x + x )

2

3

4

3

4

2

2

6

2

3

1

2

3

2

3

2

\+

x + x x +

x

4

3

4

3

2√

√

3


2

2

1

3

x1 + (x + x + x )

\+

x2 +

(x + x )

2

3

4

3

4

2

2

6

2,

3

2√

3

2√

3

2

2

2

2

1

3

6

6

2

2

\+

x3

\+

x x +

x4

−

x4

\+

3

x

4

3

4

3

12

12

2√

√

3

3

2,

2√

2

2

1

3

\=

\+

x1 + (x + x + x )

\+

x2 +

(x + x )

6

2

3

4

3

4

2

2

√

3

3

2

2

2

3

6

10

x3 +

x4

\+

x4

.

12

4

Change the variables:

⎧

1

⎪

⎪y = x + (x + x + x ),

⎪ 1

1

2

3

4

⎪

√

2

√

3

⎪

⎪

⎪

3

⎪

⎪

⎨y =

x +

(x + x ),

2

2

3

4

2

√6

6

,

2

⎪

⎪

\=

\+

12

⎪y

x3

4

x ,

⎪ 3

⎪

√3

10

⎪

⎪

⎪

⎪

⎩

y4 =

x4.

4

We obtain the quadratic form in the canonical form:

2

2

2

2

y + y + y + y .

1

2

3

4

[**10.5**](#br354)[** ](#br354)Solution.

(1) Write the matrix of quadratic form:

⎡

⎣

⎤

⎥

1

2

1

⎢

⎢

⎥

⎢

⎥ .

⎦

1

2

1





354

10 Bilinear and Quadratic Forms

Use Sylvester’s criterion. For this, compute the corner minors:



1

1






2

2

1

1

2




1

= 1 > 0,


= 1 −

\> 0.


1

2




Therefore, the form is positively deﬁnite.

(2) Write the matrix of quadratic form:

⎡

⎣

⎤

⎦

9

2

1 −

⎢

⎥

⎢

⎥

⎢

⎥ .

9

−

1

2

Use Sylvester’s criterion. For this, compute the corner minors:



9

` `1 − 






2

2

9

2




1

= 1 > 0,


= 1 −

< 0.


9

2


−

1


Therefore, the form is alternating.

(3) Assume that x3 = x4 = 0. In this case, only one non-zero summand x x

1

2

remains in the quadratic form. It is obvious that this summand can take both

positive and negative values. Therefore, the form is alternating.

(4) Assume that x = 0. In this case, only one non-zero summand x x remains

3

1 2

in the quadratic form. It is obvious that this summand can be both positive and

negative. Therefore, the form is alternating.

[**10.6**](#br355)[** ](#br355)Solution.

Write the matrix of quadratic form:

⎡

⎤

⎦

a

1

⎣

.

1 10 − a

Use Sylvester’s criterion. For this, compute the corner minors:






1



a

= a;

` `= a(10 − a) − 1.



a


1 10 − a





Answers and Solutions

355

In order for the form to be positively deﬁnite, it is necessary and sufﬁcient that both

determinants should be positive:


a > 0,

a > 0,

⇒

√

a(10 − a) − 1 > 0;

a

2 − 10 + 1 0;

a

<

⎧

⎨

a > 0,

$

√ %

⇒

⎩ ∈ 5 − 2 6 5 + 2 6

a

,

.

In order for the form to be negatively deﬁnite, it is necessary and sufﬁcient that

the corner minor of the ﬁrst order should be negative, and that of the second order

should be positive:

⎧

⎨

a < 0,

$

√

√ %

⎩ ∈ 5 − 2 6 5 + 2 6

a

,

.

This system is inconsistent; therefore, the form cannot be negatively deﬁnite at any

values of a.

Consider the cases when the corner minors are equal to zero:

2

a = 0, ω(**x**) = 2x1x2 + 10x ;

2

ω(**x**) can take a negative value, for example, at x1 = −10, x2 = 1;

√

a = 5 − 2 6,

$

√ %

$

√ %

2

2

2

ω(**x**) = 5 − 2 6 x + 2x1x2 + 5 + 2 6 x

1

\+

\+

√

2

√

2

\=

\=

5 − 2 6x1 + 2x x +

5 + 2 6x2

1

2

\+

\+

√

√

2

5 − 2 6x + 5 + 2 6x2

.

1

It is clear that ∀**x** = **0** the inequality ω(**x**) > 0 is fulﬁlled.

√

At a = 5 + 2 6, the reasoning is similar.

We obtain the ﬁnal answer: the form is positively deﬁnite if and only if a ∈

√

√ 

5 − 2 6, 5 + 2 6 .





356

10 Bilinear and Quadratic Forms

[**10.7**](#br355)[** ](#br355)Solution.

Transform the expression, having introduced integration by the auxiliary vari-

able t:

91

91

n

n

$

n

%

xixj

i + j − 1

2

j

\+ −2

xiti−1 dt.

\=

x x ti

dt =

i

j

i,j=1

i,j=1 0

i=1

0

$

%

n

2

As is easy to see, the expression

xiti−1 is always greater than zero at the

i=1

non-zero values of x , x , . . . , x and t > 0.

1

2

n

The initial quadratic form is positively deﬁnite, since it is the integral of the

positively deﬁnite form.





**Chapter 11**

**Curves of the Second Order**

The general **equation of curve of the second order** has the form

2

2

Ax + 2Bxy + Cy + 2Dx + 2Ey + F = 0,

(11.1)

where the real coefﬁcients A, B, C are not equal to zero simultaneously.

The expression Ax2 + 2Bxy + Cy2 is referred to as the **quadratic term** of the

equation of this curve, 2Dx+2Ey is referred to as the **linear term**, and F is referred

to as the **constant term**.

In the so-called **canonical system of coor[dinat](#br420)es**, the equation of curve of the

second order takes the simplest **canonical** form [[8](#br420)[\].](#br420)

Let us consider the classiﬁcation of curves of the second order based on their

canonical form.

**11.1 Ellipse**

**Ellipse** is a curve of the second order that in some Cartesian rectangular system of

coordinates is deﬁned by the equation

x2

a2

y2

b2

\+

= 1,

(11.2)

where a  b > 0. The numbers a and b are referred to as the **major** and **minor**

**semiaxes** of the ellipse, respectively.

The points (± a, 0) and (0, ± b) are called the **vertices** of the ellipse, and (± c, 0),

√

where c = a2 − b2, are its **foci**. We will denote the foci by F and F . Figure[11.1](#br367)

1

2

schematically shows an ellipse in the canonical system of coordinates.

In case of equality of the constants a = b, the ellipse degenerates into a **circle**.

© Springer Nature Switzerland AG 2021

357

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_11>





358

11 Curves of the Second Order

**Fig. 11.1** Ellipse

y

b

x2

y2

\+

= 1. The directrices

2

2

a

b

x = ± a/ε are shown by the

dotted lines

F2

F1

−a

a

x

−c

c

−b

From the geometrical point of view, the ellipse is a set of points of a plane,

for each of which the sum of distances to two speciﬁed points F and F (foci) is

1

2

constant and equal to 2a > F F . The **focal distance**, i.e. the distance between F

1

2

1

and F2, is equal to 2c.

The non-negative number ε = c/a < 1 deﬁnes the degree of “compression” of

the ellipse on the abscissa axis and is referred to as **eccentricity**. The greater is the

value ε, the more pronounced is the “compression” (see Fig. [11.2](#br367)). As is easy to see,

√

the eccentricity of the circle is equal to ε = a2 − b2/a = 0. In this connection,

we can say that the ellipse is obtained from the circle through its compression on the

Ox-axis, when the ordinates of all its points decrease in the same proportion b/a.

**Theorem 11.1** The distance from an arbitrary point P (x, y), which belongs to the

ellipse, to each focus, is equal to

r1 = PF1 = a − εx, r2 = P F2 = a + εx.

(11.3)

The ellipse has two **directrices** — the straight lines of the form x = ± a/ε. They

are shown in Fig. [11.1](#br367)[ ](#br367)as dotted lines. Directrices are not deﬁned for the circle. The

**Fig. 11.2** Ellipses with

y

different eccentricities: ε = 0

(solid line), ε = 0.7 (dotted

line), ε = 0.9 (dash-and-dot

line)

a

a

x





11.1 Ellipse

359

directrix and the focus that lie on the same side of the axis Oy will be considered to

be corresponding to each other.

**Theorem 11.2** Fo r any point that belongs to the ellipse, the ratio of its distance to

the focus to its distance to the corresponding directrix is equal to the eccentricity of

the ellipse.

Let us consider the mutual arrangement of the ellipse and the straight line. An

arbitrary straight line either does not intersect the ellipse or intersects it at one or two

points. If there is the only common point, such a straight line is a **tangent**. Exactly

one tangent passes through any point on the ellipse.

The equation of tangent to the ellipse at the point P (x , y ) has the form:

0

0

0

xx0

a2

yy0

b2

\+

= 1.

(11.4)

The ellipse has the following **optical property**: the light beams originating from

one focus, after mirror reﬂection from the ellipse, pass through another focus, i.e.

focus on it. This explains the origin of the term “focus” borrowed from optics.

Example 11.1 Let us ﬁnd the intersection points of the coordinate axes and the

x2

y2

tangent drawn to the ellipse

\+

= 1 at the point with the coordinates

9

4

√

(3/2, 3).

**Solution** Denote the tangency point by P0 and verify that it belongs to the ellipse:

√

(3/2)2 ( 3)

2

\+

= 1, or 1 = 1 — true.

(11.5)

9

4

Taking into account that the semiaxes of the ellipse are equal to a [=](#br368)[ ](#br368)3 and b = 2,

substitute the coordinates P (x , y ) into the equation of tangent ([11.4](#br368)):

0

0

0

√

(3/2)x

3y

\+

= 1.

(11.6)

9

4

√

Therefore, the general equation of straight line has the form 2x + 3 3y − 12 = 0

(see Fig. [11.3](#br369)). The intersection points of this line with the coordinate axes are (6, 0)

[√](#br369)

and (0, 4/ 3).

The idea of the ellipse as the compressed circle results in an alternative method

of specifying the ellipse **in parametric form**.

Transform the coordinates in accordance with the formulae

b

x = x, y = y.

(11.7)

a





360

11 Curves of the Second Order

y

√

2x + 3 3y − 12 = 0

P0

2

3

−

3

x

−2

x2

y2

**Fig. 11.3** To the Example [11.1](#br368)[ ](#br368)The ellipse

\+

= 1 and the tangent to it at the point

4

9

√

P0(3/2, 3)

After such a transformation, the circle x2 + y2 = a2, in the new system of

` `2

` `2

(y )

(x )

coordinates, turns into the ellipse

[+](#br422)

= 1. As is known, for example, from

2

2

a

b

the course of mathematical analysis [[76](#br422)[\],](#br422)[ ](#br422)any circle can be speciﬁed in parametric

form as

x = a cos t,

(11.8)

y = a sin t,

where the real number t takes the values that belong to the interval [0, 2π).

From ([11.7](#br368)) follows that the parametric representation of the ellipse with the

semiaxes a and b will have the form:

x = a cos t,

where 0  t < 2π.

(11.9)

y = b sin t,

The parameter t is referred to as the **anomaly of eccentricity**.

**11.2 Hyperbola**

**Hyperbola** is a curve of the second order, which in some Cartesian rectangular

system of coordinates is deﬁned by the equation

x2

a2

y2

b2

−

= 1,

(11.10)

where a, b > 0 (see Fig. [11.4](#br370)). The numbers a and b are called **real** and **imaginary**

**semiaxes** of the hyperbola, respectively.





11.2 Hyperbola

361

Unlike the ellipse, which is a connected curve, the hyperbola consists of two

connected components: left and right branches (sheets of the hyperbola).

**Vertices** of hyperbola are the points (± a, 0). **Foci** of hyperbola are the points

√

F1(−c, 0) and F2(c, 0), where c =

a

2 + 2.

b

b

A hyperbola has **asymptotes** y = ± x that deﬁne the run of the curve for

a

inﬁnitely great values of coordinates.

A hyperbola contains only those points of Cartesian plane, the modulus of the

difference of distances of each of which to the two given points F and F (foci) is

1

2

constant and equal to 2a < F F . The focal distance is equal to 2c.

1

2

For the hyperbola, a concept of **eccentricity** ε = c/a > 1 is also introduced.

**Theorem 11.3** The distances r , r from an arbitrary point P (x, y) of the hyper-

1

2

bola to each focus are equal

r1 = PF1 = abs(a − εx), r2 = PF2 = abs(a + εx).

(11.11)

The **directrices** of the hyperbola are speciﬁed in the canonical system of

a

a

coordinates by the equations x =

and x = − (see Fig. [11.4](#br370), where the

ε

ε

directrices are shown by dotted lines). The directrix and the focus that lie one the

same side of the axis Oy will be considered to be corresponding to each other.

**Theorem 11.4** For an arbitrary point that lies on the hyperbola, the ratio of its

distance to the focus to the distance to the corresponding directrix is equal to the

eccentricity of the hyperbola.

The equation of tangent to hyperbola at the point P (x , y ) has the form:

0

0

0

xx0

a2

yy0

b2

−

= 1.

(11.12)

**Optical property of hyperbola**: the light from the source situated at one of

the hyperbola’s foci is reﬂected by the second branch of the hyperbola so that the

continuations of reﬂections of the beams intersect at the second focus.

**Fig. 11.4** Hyperbola

y

x2

a2

y2

b2

−

= 1. The

b

asymptotes y = ± x are

a

shown by thin solid lines, the

a

directrices x = ± —by

F −

a F1

c

2 a

ε

dotted lines

x

−c





362

11 Curves of the Second Order

Both for the ellipse and the hyperbola, in the canonical system of coordinates,

the origin of coordinates O(0, 0) is the centre of symmetry of the curve, this is why

the ellipse and the hyperbola belong to the class of **central** curves.

In conclusion of the section devoted to the hyperbola, we will provide its

representation in parametric form:

x = ± a cosh t,

(11.13)

y = b sinh t,

where t ∈ R, cosh x = (ex + e )/2 is the hyperbolic cosine, and sinh x = (e −

−x

x

−x

e

)/2 is the hyperbolic sine. In the ﬁrst equation of this system, the sign “+”

corresponds to the right branch of the hyperbola, and the sign “−” corresponds to

the left branch.

**11.3 Parabola**

Parabola is the noncentral curve of the second order, deﬁned by the canonical

equation in Cartesian rectangular system of coordinates

y2 = 2px,

(11.14)

where p > 0 is the **focal parameter** of the parabola, or simply the **parameter**.

The **vertex** of the parabola is the origin of coordinates (0, 0), the **focus** is the

point F (p/2, 0). The **directrix** of the parabola is the straight line speciﬁed by the

equation x = −p/2 (see Fig. [11.5](#br371)).

From the geometrical point of view, the parabola is the set of the points of the

plane, for each of which the distance to the focus F is equal to the distance to the

directrix. The distance from the focus to the directrix is equal to the parameter.

**Fig. 11.5** Parabola

y

y

2 = 2 . The directrix

px

x = −p/2 is shown by a

dotted line

F

−p/2

p/

2

x





11.4 Degenerate Curves

363

**Theorem 11.5** The distance from the point P (x, y) lying on the parabola to its

focus is equal to

r = x + p/2.

(11.15)

The parabola is assigned the eccentricity equal to one.

For the parabola, the analogue of theorems [11.2](#br368)[ ](#br368)and [11.4](#br370)[ ](#br370)repeats its geometrical

property, which allows formulating the following generalized statement.

**Theorem 11.6** Fo r an arbitrary point that lies on the ellipse, hyperbola or

parabola, the ratio of the distance from this point to the focus to the distance

to the corresponding directrix (to the only directrix in case of parabola) is equal to

the eccentricity of the curve.

The equation of tangent to parabola at the point P (x , y ) has the form:

0

0

0

yy0 = p(x + x0).

(11.16)

**Optical property of parabola**: the light beams originating from the focus, after

mirror reﬂection from the parabola, will be directed parallel to its axis of symmetry.

Note that this property of parabola underlies the arrangement of parabolic mirrors

and parabolic antennas.

**11.4 Degenerate Curves**

Among the **degenerate** curves of the second order are the curves whose canonical

form is different from the equation of ellipse, parabola or hyperbola. There exist the

following types of such curves: imaginary ellipse, pair of intersecting lines, pair of

imaginary intersecting lines, pair of parallel lines, pair of imaginary parallel lines

and pair of coincident lines. Thus, **nondegenerate** curves of the second order are

ellipse, hyperbola and parabola (and they alone).

**11.4.1 Imaginary Ellipse**

Imaginary ellipse is described in the canonical system of coordinates by the equation

x2

a2

y2

b2

\+

= −1,

(11.17)

where a  b > 0.

Since the sum of squares of real numbers cannot be equal to a negative number,

this curve contains no points. The term “imaginary ellipse” is associated with the





364

11 Curves of the Second Order

√

fact that when changing the variables x = ix, y [=](#br366)[ ](#br366)iy, where i = −1, in the new

coordinates we obtain the equation of ellipse ([11.2](#br366)).

**11.4.2 Pair of Intersecting Lines**

The equation of the form

x2 y2

a2

−

= 0

b2

(11.18)

corresponds to the pair of intersecting lines. Their intersection point is the origin of

coordinates.

Having written the Eq. ([11.18](#br373)) in the form

$

% $

%

x

a

y

b

x

a

y

b

−

\+

= 0,

(11.19)

we conclude that it is satisﬁed by all points of two lines y = bx/a and y = −bx/a

intersecting at the origin of coordinates.

**11.4.3 Pair of Imaginary Intersecting Lines**

Pair of imaginary intersecting lines is described by the equation

x2

a2

y2

b2

\+

= 0.

(11.20)

The sum of squares is equal to zero if and only if each of the summands is equal

x

y

to zero: = 0 and = 0, i. e. x = y = 0. This condition speciﬁes the only point

a

b

that coincides with the origin of coordinates.

**11.4.4 Pair of Parallel Lines**

The equation

2

2

x − a = 0, where a = 0,

(11.21)

deﬁnes two parallel vertical lines x = a and x = −a.





11.5 Algorithms for Computing the Coordinates of the Tangent Points of. . .

365

**11.4.5 Pair of Imaginary Parallel Lines**

The curve of the second order, speciﬁed in the canonical system of coordinates by

the equation

2

2

x + a = 0

(11.22)

under condition a = 0, contains no real points.

**11.4.6 Pair of Coincident Lines**

And the ﬁnal type of the general equation of curve of the second order is

x2 = 0.

(11.23)

This equation is satisﬁed by the coordinates of all points lying on the ordinate axis.

As a result, based on the canonical form of curves of the second order, they are

subdivided into nine above classes, the most practically important being ellipse,

hyperbola and parabola.

**11.5 Algorithms for Computing the Coordinates of the**

**Tangent Points of Second Order Curve and the Straight**

**Line**

x2

a2

Consider a nondegenerate curve of the second order, for example, the ellipse

\+

y2

= 1, and an arbitrary point of Cartesian plane P (x , y ). Let us provide the

1

1

1

2

b

algorithm that computes the coordinates of the tangency points of the said curve

and the lines passing through P1 (see Fig. [11.6](#br375)).

We will begin with deducing the analytical relations for the coordinates of

the sought points. Denote the tangency points by T (x , y ) and T (x , y ). In

1

t1 t1

2

t2 t2

Chap. [7](#br287)[ ](#br287)“Equation of a Straight Line on a Plane” it is shown that the equation of the

family of lines passing through the set point P (x , y ) can be written in the form

1

1

y − y1 = k(x − x1), where k < ∞ is the slope. The case of a vertical tangent will

be discussed separately.





366

11 Curves of the Second Order

**Fig. 11.6** Tangents to the

y

x2

y2

P1

ellipse

\+

= 1, passing

2

2

a

b

through a point P

T1

1

T2

−a

b

a

x

−b

It is known that the tangent to the ellipse intersects it exactly at one point (see

page [359](#br368)). Therefore, the unknown slope k takes such a value that the nonlinear

system of equations

⎧

⎨ −

\=

−

y

x

a

y1 k(x x1),

2

2

(11.24)

y

⎩

\+

= 1

2

b2

has a unique solution. Having substituted the ﬁrst equation of this system into the

second one, we obtain the quadratic equation

2

2

2

2

2

2

2

2 2

(a k + b )x − 2a k(kx1 − y1)x + a (kx1 − y1) − a b = 0.

(11.25)

The necessary and sufﬁcient condition for the quadratic equation to have the only

root is the discriminant’s equality to zero

$

% $

%

4

2

2

2

2

2

2

b2 − (kx1 − y1)2

D = a k (kx1 − y1) + a a k + b

$

%

= a2b2 a k + b − (kx − y ) = 0.

2

2

2

2

(11.26)

1

1

Solution of the equation D = 0 relative to the variable k allows writing the values

of the slope:

\+

x1y1 ± b x

2

2 +

a y

2

2 −

a b

2 2

1

1

k =

.

(11.27)

x

2 −

a2

1

Further, let us consider three cases depending on the mutual arrangement of the

point P1 and the ellipse.





11.5 Algorithms for Computing the Coordinates of the Tangent Points of. . .

367

2

1

2

1

x

y

\1. The point P1 lies inside the ellipse, i.e.

\+

< 1. The radical expression

2

2

a

b

2

2 +

2

2 −

2

2 in ([11.27](#br375)) is negative, and there are no real in this case.

x b

y a

a b

k

1

1

Therefore, it is impossible to draw a tangent through the point P , which is

1

situated inside the ellipse.

2

1

a2

2

1

b2

x

y

\2. The point P1 lies on the ellipse, i.e.

x1y1

\+

= 1. Then the Eq. ([11.26](#br375)) has the

only root k =

, and P1 is a tangency point.

2

2

x − a

1

2

1

2

2

1

x

a

y

b

\3. The point P1 lies outside the ellipse,

\+

\> 1. In this case, there are two

2

possible values of k that satisfy two tangents. We will ﬁnd the coordinates of the

tangency points by substituting ([11.27](#br375)) into the Eq. ([11.25](#br375)):

a2k(kx1 y1)

−

b2(kx1 y1)

−

x 1 2 =

,

yt1,2 = −

.

(11.28)

t ,

2

2

2

2

2 2

b + a k

b + a k

Now, let us consider a special case when x1 = ± a, and one of the tangents is

vertical (see Fig. [11.7](#br376)).

In this case, one of the tangency points has the coordinates (a, 0) or (−a, 0), and

the second one is computed based on the equation D = 0, which leads to the condi-

2

2

$

2

2

1

2

1

2

%

y − b

b − y

2b y

1

1

2

1

tion k = ±

and, consequently, to the coordinates ± a

,

,

2ay

2 +

b2 +

1

b

y

y

if y = 0, and to the equation x = ± a, if y = 0.

1

1

As a result, we formulate the algorithm for ﬁnding the coordinates of the

tangency points of the straight line and the ellipse.

2

1

2

1

x

y

\1. If

\2. If

\+

\+

< 1, then there are no tangency points.

a2

b2

2

1

2

1

x

y

= 1, then there is the only tangency point (x , y ).

1

1

a2

b2

**Fig. 11.7** Tangents to the

y

x2

y2

ellipse

\+

= 1, when

2

2

a

b

P1

one of the them is vertical

b

−a

a

x

−b





368

11 Curves of the Second Order

\3. If x = ± a, then there are two tangency points

1

$

2

2

1

2

1

2

%

b − y

2b y

1

2

1

(x1, 0) and ± a

,

.

b

2 +

y

b

2 +

y

In all other cases, k and k are calculated by the formulae:

1

2

\+

\+

x1y1 + b x

2

2 +

a y

2

2 −

a b

2

2

x1y1

−

b x

2

2 +

a y

2

2 −

a b

2 2

1

1

1

1

k1 =

, k2 =

,

x

2 −

a2

x

2 −

a2

1

1

(11.29)

and the sought tangency points will have the coordinates:

2

3 2

3

a2k1(k1x1 y1)

−

b2(k1x1 y1)

−

a2k2(k2x1 y1)

−

b2(k2x1 y1)

−

, −

,

, −

b2 + a k

.

b2 + a2k1

2

b2 + a k

2

2

1

b2 + a2k2

2

2

2

2

(11.30)

Example 11.2 Let us apply the above algorithm to the values of the parameters

a = 8, b = 5 and P1(6, 5). We obtain the coordinates of the two points of tangency:


192 7

T1

,

and T2(0, 5).

25

5

**Review Questions**

\1. Write the general equation of a curve of the second order.

\2. What curve is called an ellipse?

\3. What is the eccentricity of an ellipse?

\4. Deﬁne directrices of an ellipse.

\5. Tell about the optical property of an ellipse.

\6. What curve is called hyperbola?

\7. What is the eccentricity of a hyperbola?

\8. Deﬁne directrices of a hyperbola.

\9. Tell about the optical property of a hyperbola.

\10. What curve is called parabola?

\11. What is the eccentricity of a parabola?

\12. How are directrices of a parabola deﬁned.

\13. Tell about the optical property of a parabola.

\14. Write the equation of a tangent to ellipse, hyperbola and parabola.

\15. What curves of the second order are referred to as degenerate ones?





Problems

369

**Problems**

x2 y2

**11.1**. For the ellipse

\+

= 1, compute the eccentricity and write the equation

9

18

of directrices.

x2 y2

**11.2**. Find the shortest distance from the ellipse

\+

= 1 to the line:

3

4

(1) x + 2y − 5 = 0;

(2) 2x + y − 5 = 0.

**11.3**. The ellipse x2 + 4y2 = 5 is given. Find the equation of the line that is

tangent to this ellipse at the point with the coordinates x = 1, y = −1.

**11.4**. Find the angle between the tangents drawn from the point (−8, 2) to the

2

2

x

y

ellipse

\+

= 1.

24 12

x2 y2

a2 b2

∗**11.5.** From what points of Cartesian coordinate plane is the ellipse

\+

= 1

seen at a right angle?

**11.6**. The semiaxes of an **equilateral hyperbola** are equal: a = b. Find the

eccentricity of the equilateral hyperbola.

x2

y2

**11.7**. Find the angle between the asymptotes to the hyperbola

−

= 1.

2

2

a

b

**11.8**. Find the distance from the point (4, 0) to the curve y2 − 2x = 0.

**11.9**. Write the equation of tangent to the parabola y2 = 5x at the point nearest

to the point M (2, 1/2).

0

**11.10**. The representation of hyperbola in parametric form ([11.13](#br371)) has a dis-

advantage consisting in that its left and right branches are described by

different expressions with different signs. Find the parametric speciﬁcation

of hyperbola that does not have the said disadvantage.

∗**11.11.** Assume that it is known that the line Ax + By + C = 0 is tangent to

the ellipse whose focal distance is equal to 2c. Set up the equation of this

ellipse.

x2 y2

**11.12**. Find at what points the line −3x +3y −2 = 0 and the ellipse

\+

= 1

4

2

intersect.

√

**11.13**. At what points do the line x − 3y − 2 + 3 3 = 0 and the hyperbola

x

2 − 2 = 1 intersect?

y

√

**11.14**. At what points do the line x + y − 5 5 = 0 and the parabola y2 = 6x

intersect?

**11.15**. The eccentricity of Mercury’s orbit is equal to 0.2; the major semiaxis is

equal to 0.39 astronomical units (a. u.). Compute the greatest and the least

distances of the planet from the Sun.

**11.16**. The eccentricity of the Earth’s orbit is equal to 0.017; the major semiaxis is

equal to one astronomical unit. What are the greatest and the least distances

from the Earth to the Sun?





370

11 Curves of the Second Order

**Fig. 11.8** The region

bounded by the ellipse and

the right branch of the

hyperbola

y

b

M(x , y )

m

m

∗

−a

−α

α

a

x

−b

**11.17**. Assume that it is known that the eccentricity of the ellipse is ε = 1/2. In

the canonical system of coordinates, one of its directrices is speciﬁed by the

equation x = 12. Compute the distance in this coordinate system from the

point M of the ellipse with the abscissa equal to −1 to the focus unilateral

1

with this directrix.

**11.18**. Assume that it is known that the eccentricity of the hyperbola is ε = 3/2. In

the canonical system of coordinates, one of its directrices is speciﬁed by the

equation x = −4. Compute the distance from the point N of the hyperbola

1

with the ordinate equal to 9 to the focus unilateral with this directrix.

x2

a2

y2

b2

∗**11.19.** Find the area of the regions bounded by the ellipse

\+

= 1 and the

2

2

x

y

right branch of the hyperbola

region is colour-highlighted).

−

= 1 (see Fig. [11.8](#br379), where the said

α2

β2

**Answers and Solutions**

[**11.1**](#br378)[** ](#br378)Solution.

√

The semiaxes of the ellipse are equal to a = 18 and b = 3. Compute the

eccentricity of the ellipse:

√

a

√

2 −

a

b2

18 − 9

1

c

ε =

\=

\=

√

= √ .

2

a

18

Write the equations of directrices:

a

x = ± or x = ± 6.

ε





Answers and Solutions

371

[**11.2**](#br378)[** ](#br378)Solution.

(1) Find the equations of two lines tangent to the ellipse and parallel to the line

x + 2y − 5 = 0. For this, write the equation of tangent to the ellipse:

x0x

a2

y0y

b2

\+

= 1,

where (x , y ) is the point of tangency, a2 = 4, b2 = 3. Thus, the equation of

0

0

tangent takes the form:

3x0x

4y0

3

y = −

\+

.

y0

1

The slope of the line x + 2y − 5 = 0 is equal to k = − . As is known,

2

the slopes of parallel lines coincide. Therefore, the following equality is valid:

3x x

1

0

−

= − . Moreover, the point (x , y ) belongs to the ellipse. As a result,

2

0

0

4y

0

we obtain the system of equations:

⎧

3x0

1

2

⎪−

= −

⎨

,

4y0

2

2

⎪x

y

⎩

0

0

\+

= 1.

3

4

The set of its solutions has the form {(1, 3/2) , (−1, −3/2)}.

We obtain the equations of tangents:

x + 2y − 2 = 0, x + 2y + 2 = 0.

Note that the ﬁrst of them is located closer to the initial line, since the

following inequality is valid: abs((−2) − (−5)) < abs(2 − (−5)) (see

Problem [**7.13**](#br301)).

It only remains to ﬁnd the distance from the point (1, 3/2) to the line x +

2y − 5 = 0.

Let us use the formula ([7.37](#br296)):

3

√

abs(1 · 1 + 2 · − 5)

abs(Ax + By + C)

5

0

0

2

d = abs(δ) =

√

\=

√

\=

5

.

A

2 +

B

2

12 + 22

x2 y2

So, the shortest distance from the ellipse

\+

= 1 to the line x+2y−5 =

3

4

√

5

0 is equal to

.

5





372

11 Curves of the Second Order

(2) Find the equations of two lines, tangent to the given ellipse and parallel to the

line 2x + y − 5 = 0. Similarly to the previous item of this problem, we obtain

the system of equations relative to the unknown coordinates of the tangency

point x and y :

0

0

⎧

3x0

4y0

⎪−

= −2

⎨

,

2

2

⎪x

y

⎩

0

0

\+

= 1.

3

4

:



;

8

3

8

3

We obtain the set of solutions

√

, √

19

, −√ , −√

. Find the

19

19

19

equation of the tangents:

√

√

y = −2x + 19, y = −2x − 19.

Note that the ﬁrst of them is closer to the initial line, since the following

√

√

inequality is valid: abs(− 19−(−5)) < abs( 19−(−5)) (see Problem [**7.13**](#br301)).


8

3

The distance from the point

√

, √

to the line 2x + y − 5 = 0 will

19

19

be found by the formula ([7.37](#br296)):

8

3

√

√

abs(2 · √ + 1 · √ − 5)

19 19

abs(Ax + By + C)

5 5 − 95

.

0

0

d =

√

\=

√

\=

A

2 +

B

2

22 + 12

5

x2

y2

As a result, the shortest distance from the ellipse

\+

= 1 to the line

3

4

√

1√

2x + y − 5 = 0 is equal to 5 −

\95.

5

[**11.3**](#br378)[** ](#br378)Solution.

Use the equation of tangent to ellipse ([11.4](#br368)):

xx0

a2

yy0

b2

\+

= 1.

5

In our case, a2 = 5, b2 = , x = 1, y = −1, and the equation of tangent takes

0

0

4

x · 1 y · (−1)

the form

\+

= 1, or x − 4y − 5 = 0.

5

5/4

[**11.4**](#br378)[** ](#br378)Solution.

According to the problem statement, through the point (−8, 2) pass both tangents

to the ellipse.





Answers and Solutions

373

As is shown in Sect. [11.5](#br374)[ ](#br374)(formula ([11.27](#br375))), the slopes of the tangents k1 and k2

are computed by the formula

\+

x1y1 ± b x

2

2 +

a y

2

2 −

a b

2 2

1

1

k1,2 =

.

2

2

x − a

1

We obtain k [=](#br291)[ ](#br291)1/5, k = −1.

1

2

Based on the ([7.17](#br291)), we ﬁnd the angle between the lines.

k1 − k2

1 + k k

1/5 − (−1)

3

2

ϕ = arctan

= arctan

2

\=

.

1 + (1/5)(−1)

1

3

2

Therefore, the angle between the tangents to the ellipse is equal to ϕ = arctan

[**11.5**](#br378)[** ](#br378)Solution.

.

Since the ellipse seen at a right angle from some point M(x, y), then the angle

between the tangents drawn from M to the ellipse is equal to π/2. Based on the

formula ([11.27](#br375)) on page [366](#br375)[ ](#br375)the slopes of the tangents k and k are equal to

1

2

\+

x1y1 ± b x

2

2 +

a y

2

2 −

a b

2 2

1

1

k1,2 =

.

2

2

x − a

1

Compute the angle ϕ between the tangents using the equation ([7.17](#br291)):

k1 − k2

tan ϕ =

,

1 + k k

1

2

therefore,

\+

2 b2x + a y − a b

2

2

2

2 2

k1 − k2

1

1

ϕ = arctan

= arctan

.

1 + k k

2 + 2 −

a2 −

2

1

2

x

y

b

1

1

It follows from the obtained equation that the angle ϕ = π/2, if the denominator of

fraction under the arctangent is equal to zero: x2 + y2 − a2 − b2 = 0.

1

1

2

2

2

x

a

y

As a result, the ellipse

\+

= 1 is seen at a right angle from all points of the

b2

plane that satisfy the equation

2

2

2

2

x + y = a + b .

√

Such points, as is easy to see, form a circle of radius a2 + b2.





374

11 Curves of the Second Order

[**11.6**](#br378)[** ](#br378)Solution.

√

c

The eccentricity of the hyperbola is equal to ε = , where c = b2 + a2 is half

a

of the interfocal distance, a, b are semiaxes of the hyperbola.

If a = b, then

√

√

a

2 +

a

a2

2 +

a

a2

√

\2.

b

ε =

\=

\=

√

Thus, we obtain that the eccentricity of the equilateral hyperbola is equal to 2.

[**11.7**](#br378)[** ](#br378)Solution.

x2

a2

y2

b2

The asymptotes to the hyperbola

−

= 1, as is known (see page [361](#br370)),

b

b

are deﬁned by the equations y = ± x. The slopes of these lines are equal to ±

.

a

a

Therefore, the tangent of half of the angle α between the asymptotes is equal to

b

tan(α/2) = . Let us express, from the obtained relation, the sought angle:

a

b

α = 2 arctan

.

a

Note that for the equilateral hyperbola (see Problem [**11.6**](#br378)), the angle between the

asymptotes is equal to π/2.

[**11.8**](#br378)[** ](#br378)Solution.

In order to ﬁnd the distance from the point (x , y ) to the curve y2 − 2x = 0,

0

0

ﬁnd the least value of the functions

\+

d1(x) = (x − x0)2 + (f1(x)

−

y0)2 and

\+

d2(x) = (x − x0)2 + (f2(x) y0)2,

−

√

where x = 4, y = 0, and by f1,2(x) = ± 2x are denoted two branches of the

0

0

2

parabola y − 2x = 0.

\-

First, consider the function d (x): d (x) = (x − 4)2 + 2x. Its derivative is

1

1

x − 3

1

equal to d (x) = -

. The point suspected of being the extremum is

(x − 4)

2 + 2

x

the solution of the equation d (x) = 0, or x − 3 = 0. This is the minimum point.

\-

1

√

Therefore, min d (x) = (3 − 4)2 + 2 · 3 = 7.

1

√

Similarly, we ﬁnd the least value of the function d (x): min d (x) = 7.

2

2

As a result, we obtain that the distance from the point (4, 0) to the parabola is

√

equal to 7.

[**11.9**](#br378)[** ](#br378)Answer:

√

5x − 2 10y + 10 = 0.





Answers and Solutions

375

[**11.10**](#br378)[** ](#br378)Answer:

⎧

⎨

a

x =

,

cos t

y = b tan t,

⎩

where t ∈ (0, 2π).

[**11.11**](#br378)[** ](#br378)Solution.

Denote the tangency point by P(x , y ). The equation of tangent to ellipse at this

0

0

point has the form:

xx0

a2

yy0

\+

= 1,

b2

where a and b are the major and minor semiaxes of the ellipse, respectively. On the

other hand, according to the problem statement, the general equation of line has the

form Ax + By + C = 0, and it can be rewritten as

$

%

$

%

A

C

B

C

−

x +

−

y = 1.

x0

A y0

B

Comparing the obtained equations, we obtain

= −

,

C b

= − , therefore,

2

2

a

C

the coordinates of the tangency point P are equal to −Aa2/C, −Bb2/C . It is clear

2

0

2

0

x

y

that the coordinates of the point P satisfy the equation of the ellipse

\+

= 1.

2

2

a

b

Moreover, from the deﬁnition of focus follows the equality a2 − b2 = c2, where

c is the focal parameter. Hence, we obtain the system of equations relative to the

parameters a, b:

⎧

$

2 %

$

2 %

1

a2

Aa

C

2

1

b2

Bb

C

2

⎨

−

\+

−

= 1,

⎩

2 −

b2 = c ,

2

a

or:

⎧

2

2

b2B2

C2

⎨a A

\+

= 1,

2

C

2 −

⎩

a

b2 = c2.

$

2

2

2 %

$

2

2

2 %

C − c B

1/2

C

−

c A

B2

1/2

The solution of this system is: a =

, b =

.

2 +

B

2

A

2 +

A





376

11 Curves of the Second Order

Thus, the sought equation of ellipse has the form:

2

2

2

2

A + B

A + B

x2 +

C

y2 = 1.

2

2

2 −

2

2

C

2 −

c B

c A

[**11.12**](#br378)[** ](#br378)Solution.

2

Express y from the equation of line: y = x +

Substitute y into the equation of ellipse:

.

3


x2

1

4

4

9

4

3

\+

\+

· x + x2 = 1,

2

8

14

9

4

2

3

2

or 27x + 12x − 32 = 0, hence, we obtain x = , y =

; x = − , y = − .

1

1

2

2

9

3

So, the intersection points of the line and the ellipse are (8/9, 14/9),

(−4/3, −2/3).

[**11.13**](#br378)[** ](#br378)Solution.

√

Express the variable x: x = 3y + 2 − 3 3.

In order to ﬁnd the points at which the line and the hyperbola intersect, substitute

the obtained expression for x into the equation of hyperbola:

√

√

2

2

9y + 6y(2 − 3 3) + 31 − 12 3 − y − 1 = 0,

or

$

√ %

√

2

8y + y 12 − 18 3 + 30 − 12 3 = 0,

√

√

5 3 − 6

3 3 − 10

√

√

hence: y1 =

, x1 =

; y = 3, x2 = 2.

2

4

4

√

$

%

√

3 3 − 10 5 3 − 6

Thus, the sought intersection points are

,

, (2, 3).

4

4

[**11.14**](#br378)[** ](#br378)Solution.

In order to ﬁnd the intersection points of the line and the parabola, solve the

system of equations:

⎧

⎨

⎧

⎨

√

√

√

x + y − 5 5 = 0,

x = −y + 5 5,

2

⇒

√

⇒ y + 6y − 30 5 = 0,

⎩

2

⎩

2

y = 6x

y = −6y + 30 5

The obtained quadratic equation has the roots

\+

√

y1,2 = −3 ± 9 + 30 5.





Answers and Solutions

377

√

Substitute the values y1,2 into the equation of a straight line x + y − 5 5 = 0. We

obtain

\+

√

√

x1,2 = 3 ∓ 9 + 30 5 + 5 5.

Thus, the coordinates of the intersection points are:

\-

√

√

\-

√

M1(3 − 9 + 30 5 + 5 5, −3 + 9 + 30 5),

\-

√

√

\-

√

M2(3 + 9 + 30 5 + 5 5, −3 − 9 + 30 5).

[**11.15**](#br378)[** ](#br378)Solution.

According to the ﬁrst law of Kepler,[1](#br386)[ ](#br386)all planets of the S[olar](#br420)[ ](#br420)system move along

an ellipse, in one of the foci of which the Sun is situated [[10](#br420)[\]](#br420). The closest to the

Sun point of the orbit P is referred to as the perihelion, and the farthest from the

Sum point of the orbit A is referred to as the aphelion.

In order to compute these values for the planet Mercury, introduce the notations:

F1(c, 0) are the coordinates of the Sun, P (a, 0) are the coordinates of the perihelion,

A(−a, 0) are the coordinates of the aphelion and O(0, 0) is the centre of symmetry

of the ellipse. Here, a is the major semiaxis, and c is the focal parameter.

Then:

ra = AF1 — the greatest distance from Mercury to the Sun,

rp = PF1 — the least distance from Mercury to the Sun,

c = OF1.

Geometrically, we obtain

a = rp + c,

a = ra − c;

rp = a − c,

ra = a + c;

⇒

The eccentricity of the ellipse ε will be computed by the formula:

√

a

2 −

a

b2

ε =

,

√

where a2 − b2 = c,

c

ε = ⇒ c = aε.

a

1Johannes Kepler (1571–1630), German mathematician and astronomer.





378

11 Curves of the Second Order

Hence,

rp = a − aε,

ra = a + aε;

rp = a(1 − ε),

ra = a(1 + ε).

Substitute the numeric values from the problem statement:

r = 0.39 · (1 − 0.2) ⇒ r = 0.312 (a. u.),

p

p

r = 0.39 · (1 + 0.2) ⇒ r = 0.468 (a. u.).

a

a

So, the greatest distance from Mercury to the Sun is equal to 0.468 a.u., the least

distance is equal to 0.312 a.u.

[**11.16**](#br378)[** ](#br378)Solution.

Denote the points F1(c, 0) as the coordinates of the Sun, P (a, 0) as the

coordinates of the perihelion, A(−a, 0) as the coordinates of the aphelion, O(0, 0)

as the centre of symmetry of the ellipse. Here, a is the major semiaxis, and c is the

focal parameter of the Earth’s orbit. Then (see previous problem):

ra = AF1,

rp = PF1,

c = OF1;

⇒

rp = a(1 − ε),

ra = a(1 + ε);

where ε = 0.017 is the eccentricity of the Earth’s orbit, a = 1 a.u.

Perform the necessary computations:

r = 1 · (1 − 0.017) ⇒ r = 0.983 (a. u.),

p

p

r = 1 · (1 + 0.017) ⇒ r = 1.017 (a. u.).

a

a

As a result we obtain that the greatest distance from the Earth to the Sun is equal to

1.017 a.u., and the least distance is equal to 0.983 a.u.





Answers and Solutions

379

[**11.17**](#br378)[** ](#br378)Solution.

The point M has the coordinates (−1, y ) and is situated on the left of Oy-

1

1

axis, and the focus is on the right. The sought distance is equal to the length of the

hypotenuse r of the triangle with the vertices F (c, 0), M (−1, y ) and L(−1, 0).

1

1

1

According to the Pythagorean theorem:

\+

r = (c + 1)2 + y .

2

a

Using the deﬁnition of directrix of ellipse x = ± , we ﬁnd

ε

a

xd =

,

⇒

a = εxd,

ε

where, according to the problem statement, x = 12.

d

Express the focal parameter c of the ellipse:

2

c = aε = ε x .

d

(−1)

2

The coordinate y1 will be determined using the equation of the ellipse

\+

2

a

2

1

b2

y

= 1:

\-

b

a

y1 = ±

a2 − 1

.

Since for the ellipse the following relation is valid: b2 = a2 − c2 = a2(1 − ε2),

then

\-

y1 = ± (1 − ε2)(a2 − 1).

Therefore, the length of the hypotenuse F M of the triangle F LM is equal to

1

1

1

1

\+

\-

r = (c + 1)2 +

y

2 =

(aε

\+ 1 2 + 1 −

)

(

ε2)(a

2 − 1 =

)

a

\+

ε

\=

ε(xd

\+ 1

).

1

Substitute here the numeric values from the problem statement, and we obtain the

13

ﬁnal answer: r =

[**11.18**](#br379)[** ](#br379)Solution.

.

2

The sought distance is equal to the length of the hypotenuse of the triangle with

the vertices F (−c, 0), N (x , y ) and L(x , 0), where, according to the problem

2

1

1

1

1

statement, y = 9. Depending on whether the point N (x , y ) is situated on the

1

1

1

1





380

11 Curves of the Second Order

right or on the left branch of the hyperbola, we obtain two possible values of r:

\+

r = (x1 ± c)2 + y .

2

1

a

According to the deﬁnition of directrix of the hyperbola x = ± , we have

ε

a = ε abs(x ), where x = −3.

d

d

The parameter c of the hyperbola is equal to

2

c = aε = ε abs(x ).

d

(−1)

2

2

1

b2

y

Since

−

= 1 and c = a − b , then

2

2

2

2

a

2


x

2

2

2

1

2

2

2

r = (x1 ± c) + b

− 1 = (a ± εx1) = ε (abs(x ) ± x1) ,

a2

d

.

\+

2

1

a

b

y

where x1 =

y12 + b2 =

\+ ε x . Having substituted the values from

2 2

d

ε2 − 1

,

,

14

5

14

5

the problem statement, we obtain r = 9

\+ 6 or r = 9

− 6.

[**11.19**](#br379)[** ](#br379)Solution.

Denote the region bounded by the ellipse and the hyperbola by D. Due to the

properties of symmetry of ellipse and hyperbola, the sought area is expressed as the

doubled area of the region D0:

S(D) = 2S(D0).

In Fig. [11.8](#br379)[ ](#br379)the region D is marked with the symbol “∗”.

0

The equation of the part of the ellipse lying in the ﬁrst quadrant has the form

√

b

yell =

a

2 −

x2, where 0 < x < a.

a

The equation of the part of the right branch of the hyperbola, which is situated

√

β

above the abscissa axis, is: yhyp

\=

α2 − x2, where x > α.

α

Assume that xM is the abscissa of the point M of intersection of the curves y

and yhyp, which point lies in the ﬁrst quadrant.

ell

Note that when the condition a  α is satisﬁed, such a point always exists.

Otherwise, when a < α, the region D is empty, and S(D) = 0.





Answers and Solutions

381

So, under the condition a  α, the following equality is valid:

9

9

xM

a

S(D0) =

yhyp(x) dx +

yell(x) dx.

(11.31)

α

xM

Compute the coordinate xM :

\+

\+

b

a

β

α

yell(x ) = yhyp(x ) ⇒

a2 −

x

2 =

x

2 −

a .

2

M

M

M

M

Solution of this equation that satisﬁes the conditions x > 0, y > 0, has the form:

.

b

2 +

β2

xM = aα

.

a β + b α

2

2

2

2

Substitution of xM into the formula ([11.31](#br390)) for S(D0) results in:

⎡

.

1

2

β

α

a2 + α2

b2 + β2

S(D0) =

⎣

ab

arctan

⎛ .

.

⎞ ⎤

a

2 −

α2

α2b2

b

a2β

2 +

2 +

β2

α2b2

−αβ ln ⎝b

\+ a

⎠ ⎦ .

a2β

2 +

Finally, we obtain the area of the region bounded by the ellipse and the right

branch of the hyperbola:

⎧

⎪0 if

α,

⎪ ,

a

⎪

⎪

⎪

⎪

.

⎪

⎪

⎪

2 +

2 +

α2

β2

⎨

β

α

a

b

ab arctan

−

S(D) =

⎪

⎛

⎞

⎠

⎪

.

.

⎪

⎪

⎪

2 −

α2

2 +

2 +

β2

⎪

a

b

⎪ −

ln ⎝

\+

, a > α.

if

⎪

αβ

b

a

⎪

⎩

a2β

2 +

α2b

2

a2β

α2b

2





**Chapter 12**

**Elliptic Curves**

**Elliptic curve** is a plane curve that has no singular points and is deﬁned by an

equation of the form

2

3

y = x + ax + b,

(12.1)

where a and b are real numbers. The requirement of absence o[f](#br391)[ ](#br391)singular points

means that the curve must not have any self-intersection and cusps[.](#br391)[1](#br391)[ ](#br391)This condition

will be satisﬁed if and only if the **discriminant** of the equation

3

2

` `= −16(4a + 27b ) = 0

(12.2)

is other than zero. Of course, the constant factor 16 does not inﬂuence the sign of

the discriminant; this factor is introduced for convenience of investigation of further

and deeper properties of the curve.

The name “elliptic curve” goes back to the problem of computing the length of

the ellipse arc, leading to computation of the deﬁnite integral of the form

9

x2

R(x)

√

dx

(12.3)

x3 + ax

\+

b

x1

for some rational function R(x) [[7](#br420)[,](#br420)[ ](#br420)[32](#br421)[\].](#br421)[ ](#br421)Morphological similarity of the terms

“ellipse” and “elliptic curve” is due to historic reasons. Let us emphasize that these

terms belong to different mathematical concepts.

1An example of self-intersection see on Fig. [12.6](#br411)[ ](#br411)at page [403](#br411). An example of a cusp is shown on

Fig. [12.1](#br393)e at page [385](#br393).

© Springer Nature Switzerland AG 2021

383

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3_12>





384

12 Elliptic Curves

As a [sphere](#br392)[ ](#br392)of application of elliptic curves, we should mention the proof of

Fermat’[s](#br392)[2](#br392)[ ](#br392)Last Theorem and the discovery of a new and rapidly developing scientiﬁc

ﬁeld about the conﬁdential data transfer methods—elliptic-curve cryptography.

There are other known applications [of](#br420)[ ](#br420)[su](#br420)[ch](#br420)[ ](#br420)curves in mathematics and adjacent

ﬁelds, in particular, in number theory [[13](#br420)[,](#br420)[ ](#br420)[14](#br420)[\].](#br420)

Depending on the sign of the discriminant, the elliptic curve is formed by one or

two connected components:

• if  > 0, then the curve graph consists of two connected components;

• if  < 0, then the curve graph consists of one connected component.

Note If the conditions  = 0 and a = 0 are satisﬁed, a point of self-intersection

appears on the curve, and if the equalities a = b = 0 occur, then a cusp appears.

Example 12.1 In Fig. [12.1](#br393)[ ](#br393)are shown several elliptic curves for the values of

the parameters a ∈ {−4, 0, 4}, b ∈ {−2, 0, 2}. Note that at a = b = 0 we obtain the

equation y2 = x3, for which  [=](#br393)[ ](#br393)0, therefore, such a curve does not belong to the

class of elliptic curves. In Fig. [12.1](#br393)[ ](#br393)it is located on the panel e) and is shown by the

dotted line.

**12.1 Operation of Multiplication of the Elliptic Curve Points**

Having ﬁxed two points located on an arbitrary elliptic curve  = {(x, y) ∈

R2 : y2 = x3 + ax + b}, we can deduce a rule for constructing the third point.

Such an operation will be referred to as “addition” of points on an elliptic curve.

In order to perform the operation of addition of points, the Cartesian plane R2

should be expanded by introducing a **point at inﬁnity** ∞. As will be clear from

the further discussion, the point ∞ has the properties of a zero element in the set

R2 ∪ {∞} with the operation of multiplication of points deﬁned on it. Due to this,

the designation O ≡ ∞ is also used for the point at inﬁnity.

Assume that any elliptic curve passes through the point O. We can say that two

vertical lines intersect at this point.

So, let the following elliptic curve be speciﬁed

2

2

3

` `= {(x, y) ∈ R : y = x + ax + b} ∪ {O}.

(12.4)

The main idea of determining the sum A ⊕ B of the two points A = (x , y )

A

A

and B = (x , y ) on the elliptic curve consists in computing the coordinates of the

B

B

intersection point of the line AB and :

C = A ⊕ B = {(x , y ): C ∈ AB and C ∈ }

(12.5)

C

C

2Pierre de Fermat (1601–1665), French mathematician and lawyer.





12.1 Operation of Multiplication of the Elliptic Curve Points

385

y

y

y

a)

b)

e)

h)

c)

x

x

x

y2 = x3 − 4x − 2

y2 = x3 − 4x

y2 = x3 − 4x + 2

y

y

y

d)

f)

x

x

x

y2 = x3 − 2

y2 = x3

y2 = x3 + 2

y

y

y

g)

i)

x

x

x

y2 = x3 + 4x − 2

y2 = x3 + 4x

y2 = x3 + 4x + 2

**Fig. 12.1** Elliptic curves for the values of the parameters a ∈ {−4, 0, 4}, b ∈ {−2, 0, 2}.

Rectangular mesh on the panels (**a**)–(**i**) has a step equal to 2. The point (0, 0) on panel (**e**) is

the cusp for the curve y2 = x3





386

12 Elliptic Curves

and the subsequent reﬂection of C relative to Ox-axis: C → C. The point C is

deemed as the sum of the points A and B; the remaining part of this section will be

devoted to the formal deﬁnition of such a summation operation.

In this case, we suppose that

\1. the vertical lines of the form x = const pass through the point at inﬁnity;

\2. if the line AB is tangent to the curve , then the tangency point is taken into

account twice.

The point on the elliptic curve, **opposite** to the point A = (x , y ), is the point

A

A

−A = (x , −y ), resulting from the reﬂection of the initial point relative to the

A

A

abscissa axis. As is easy to see, A ∈  ⇒ −A ∈  due to quadratic dependence of

the algebraic equation that deﬁnes  on the variable y.

A new rule is introduced for the point at inﬁnity: −∞ = ∞, in other words, the

point ∞ is deemed opposite to itself.

Let us proceed to the rule of computing the coordinates of the point A ⊕ B. For

this, consider four cases:

\1. addition of a point and O;

\2. addition of two different points, where A = −B;

\3. addition of the two opposite points A and −A;

\4. duplication of a point, i.e. computing the sums of the form A ⊕ A.

**12.1.1 Addition of a Point and O**

Let us deﬁne the sum of an arbitrary point A(x , y ) of the expanded Cartesian

A

A

plane and the point O as

A ⊕ O = O ⊕ A = A.

(12.6)

This means that addition of the point O does not change the values of the initial

point coordinates. As was already mentioned above, this fact allows deeming the

point at inﬁnity to be the zero element in the set R2 ∪ {∞} with the operation of

addition deﬁned on it.

**12.1.2 Addition of Two Different Points**

In order to compute the sum A ⊕ B on the condition A = −B we should ﬁnd

the intersection point of the line AB with the speciﬁed elliptic curve . Denote the



respective intersection point by C . Then we ﬁnd the point C = −C opposite to C ,

reﬂecting the point C relative to the Ox-axis. This, the coordinates of the point C

and C are connected by the relations x = x , y = −y .



C

C

C

C





12.1 Operation of Multiplication of the Elliptic Curve Points

387

**Fig. 12.2** Addition of two

different points A and B on

the elliptic curve

y

−C

B

x

A

C = A ⊕ B

The sum of the points A and B is the point C, constructed in the above manner:

C = A ⊕ B.

(12.7)

In Fig. [12.2](#br395)[ ](#br395)is shown a geometric method of constructing the point A ⊕ B.

Solution of the system

⎧

⎨ −

2 = 3 +

\+

( y )

C

x

ax

b,

C

C

y − y

(12.8)

B

A

⎩ −

( y ) yA

−

\=

−

(xC x )

A

C

x − x

B

A

reduces to solving the equation of the third degree with real coefﬁcients. Of course,

t[he](#br421)[ ](#br421)roots of such an arbitrary equation can be found using known Cardano formulae

[[41](#br421)[\];](#br421)[ ](#br421)however, in this case, we can perform easier computations.

Using Viète’s formulae (see Problem [**4.31**](#br207)), we may say that the sought coordi-

nates of the point C are determined by the formulae:

xC = 

2 −

xA x ,

B

−

(12.9)

yC = −y + (x − x ),

A

A

C

y − y

B

A

A

where the designation  =

is introduced for the slope of the line AB.

x − x

B





388

12 Elliptic Curves

**Fig. 12.3** Addition of two

opposite points A and −A

y

O = A ⊕ (−A)

A

x

−A

**12.1.3 Addition of Two Opposite Points**

Let us proceed to the case when the summands in the sum of the points are opposite

points, for example, A and −A.

Draw a line that passes through two opposite points. As can be seen from the

Fig. [12.3](#br396), such a line will be positioned vertically, and the third point, which is

common for the elliptic curve and the drawn line, can only be positioned at inﬁnity.

Based on this fact, the sum of the opposite points is deﬁned as A⊕(−A) = ∞. The

Fig. [12.3](#br396)[ ](#br396)illustrates the formulated rule.

**12.1.4 Duplication of a Point**

The computation of the sum of the points of the form A ⊕ A, i.e. **duplication of a**

**point**, will require the operation of passage to the limit:

A ⊕ A = Bl→i mA A ⊕ B.

(12.10)

Geometrically it means that we are drawing a line through two different points

A(x , y ) and B(x , y ) of the elliptic curve, and the second point lies in the small

A

A

B

B

neighbourhood of the ﬁrst one:

lim A ⊕ B = lim A ⊕ B.

(12.11)

B→A

x

→x ,

y

B A

B

A

→y





12.1 Operation of Multiplication of the Elliptic Curve Points

389

y

y

\=

a)

b)

O

A ⊕ A

A

−C

A

x

x

A ⊕ A

**Fig. 12.4** Duplication of a point A. On the panel (**a**), the case yA = 0 is schematically shown; on

the panel (**b**) the case yA = 0

As is seen from the Fig. [12.4](#br397), this case corresponds to drawing a tangent at the

point A to the elliptic curve.

Suppose that the tangent intersects the curve at the point −C. Note that if the

ordinate of the point A is equal to zero, then the said tangent will be positioned

vertically. Based on the previous case described in Sect. [12.1.3](#br396), we obtain −C = ∞,

A ⊕ A = A ⊕ (−A) = O. For all other values of the ordinate y = 0, as a result of

A

reﬂection of the point −C relative to the horizontal axis, a point C = A ⊕ A will be

constructed.

Let us write the respective analytical relations:

xC = 

2 − 2

x ,

A

(12.12)

yC = −y + (x − x ),

A

A

C

3x2 + a

where the value  =

A

2y

is equal to the tangent of the slope of the tangent line

A

relative to the horizontal axis.

Two other cases of point duplication discussed above are illustrated in Fig. [12.4](#br397)a

and b.

Analysis of the formulated addition procedure leads to the criterion of equality

O of the sum of three points.

**Theorem 12.1** A sum of three points is equal to O if and only if they lie on the same

straight line.

Example 12.2 Compute the sum (−2, −1) ⊕ (0, 1) of two points on the elliptic

curve deﬁned by the equation y2 = x3 − 4x + 1.

**Solution** Denote A = (−2, −1), B = (0, 1) and C = A ⊕B. Verify that the points

2 = 3 − 4 + 1.

A and B lie on the curve y

x

x





390

12 Elliptic Curves

Indeed,

A : (−1) = (−2) − 4 · (−2) + 1, or 1 = 1 is true,

2

3

(12.13)

(12.14)

2

3

B : 1 = 0 − 4 · 0 + 1, or 1 = 1 is true.

By deﬁnition, in order to compute the sum A⊕B we should ﬁnd the intersection

point of the line AB with the speciﬁed elliptic curve, following which we should

reﬂect the intersection point relative to Ox-axis.

Write the equation of the line that passes through two points (see Eq. ([7.12](#br290)) on

page [280](#br290)):

y − y

B

A

A

y − yA =

(x − xA),

(12.15)

x − x

B

where (x , y ) and (x , y ) are the coordinates of the initial points.

A

A

B

B

Having substituted the numeric values of the coordinates into Eq. ([12.15](#br398)), we

arrive at the equation of the line y = x + 1. The line speciﬁed by this equation

intersects the elliptic curve y2 = x3 − 4x + 1 at a point with the abscissa x , for

C

which the following equality is valid

2

3

C

(x + 1) = x − 4x + 1,

(12.16)

C

C

or

3

C

2

C

x − x − 6x = 0.

(12.17)

(12.18)

C

As is easy to see, the obtained cubic equation has the roots

(xC)1 = −2, (xC)2 = 0, (xC)3 = 3.

The ﬁrst two values satisfy the abscissas of the initial points A and B; the value

= 3 is the abscissa of the intersection point of the line AB and the elliptic curve.

x

C

Denote this point as C: x = 3.

C

Having substituted x into the equation y = x + 1, we obtain y = 4—the

C

C

ordinate of the point C.

The coordinates of the sought point C = A ⊕ B are equal to

xC = xC,

(12.19)

yC = −yC.

As a result, xC = 3, yC = −4, therefore, on the curve y2 = x3 − 4x + 1 the

following equality is valid

(−2, −1) ⊕ (0, 1) = (3, −4).

(12.20)





12.1 Operation of Multiplication of the Elliptic Curve Points

391

Note that the use of the relations ([12.9](#br395)) also leads to the desired result.

Example 12.3 Compute the sum (−2, 3) ⊕ (3, −3) of two points on the elliptic

curve speciﬁed by the equation y2 = x3 − 7x + 3.

**Solution** Verify that the points (−2, 3) and (3, −3) belong to the curve.

2

3

The ﬁrst point: 3 = (−2) − 7(−2) + 3, or 9 = 9 is true;

2

3

the second point: (−3) = 3 − 7 · 3 + 3, or 9 = 9 is true.

In order to compute the sum, use the formulae ([12.9](#br395)), into which the values

xA = −2, yA = 3, xB = 3, yB = −3 should be substituted:

−3 − 3

6

` `=

= − ,

(12.21)

3 − (−2)

5


2

6

11

25

xC

\=

−

− (−2) − 3 =

,

(12.22)

(12.23)

5



6

5

11

9

yC = − 3 +

−

−2 −

= −

.

25

125

So, by algebraic method, we have obtained the equality (−2, 3) ⊕ (3, −3) =


11

25

9

, −

.

125

For the sum of the points of the form C

\=

A ⊕ A ⊕ A ⊕ · · · ⊕ A the



!

n times

designation C = n A is used.

For n < 0 the point n A is deﬁned as the element opposite to (−n) A.

Multiplication by zero results in a point at inﬁnity O.

Thus, the point n A, which is the sum n of the points A, is deﬁned for all integral

n in accordance with the following rule:

⎧

⎪ A ⊕ A ⊕ A ⊕ · · · ⊕ A , if n > 0,

⎪

⎪



!

⎨

n times

n A =

(12.24)

⎪

O,

if n = 0,

if n < 0.

⎪

⎪

⎩

−|n|A,

Example 12.4 Compute the sum of four points 4(5, 11) on the elliptic curve,

deﬁned by the equation y2 = x3 − 2x + 6.

**Solution** Verify that the point (5, 11) belongs to the elliptic curve:

2

3

11 = 5 − 2 · 5 + 6, or 121 = 121 is true.

(12.25)

Use the equality

4(5, 11) = (5, 11) + (5, 11) + (5, 11) + (5, 11) = 2(5, 11) + 2(5, 11). (12.26)





392

12 Elliptic Curves

By the duplication formulae ([12.12](#br397)) we obtain

73

22

` `=

,

2(5, 11) = (489/484, 23835/10648).

(12.27)

Applying the duplication formula again and using a program in Python for

computing, we arrive at the ﬁnal answer:

4(5, 11) = ( − 2 160 508 643 999/1 099 855 587 600,

− 1 767 794 172 358 992 751/1 153 462 548 939 624 000). (12.28)

As is seen from the considered example, the arithmetic operations with the

elliptic curve points are in many cases very labour-intensive and it is almost

impossible to obtain the result without application of computing systems.

**Theorem 12.2** The operation of addition of the points deﬁned on the elliptic curve

` `on the set R

O has the following properties:

2 ∪ { }

\1. A ⊕ O = O ⊕ A = A ∀A ∈ ;

\2. A ⊕ (−A) = O ∀A ∈ ;

\3. A ⊕ B = B ⊕ A ∀A, B ∈ ;

\4. (A ⊕ B) ⊕ C = A ⊕ (B ⊕ C) ∀A, B, C ∈ .

The result of the operation “⊕” belongs to the same set R ∪ {O}.

2

In other words, the operation “⊕” is commutative and associative. The role of

the opposite to A is played by −A; the role of zero (neutral element) is played by

the point O = ∞.

**12.2 Elliptic Curves with Rational Points**

In the previous sections of this chapter, as the universal set was considered a

Cartesian plane completed with a point at inﬁnity ∞:

U = R2 ∪ {O}.

(12.29)

Recall that the universal set, by deﬁnitio[n,](#br421)[ ](#br421)[co](#br421)ntains the entire set of values that the

variables can take in a certain problem [[41](#br421)[\].](#br421)[ ](#br421)For cryptography and number theory,

the most signiﬁcant are the properties of the elliptic curves on the set of points with

the rational coordinates Q2 ∪ {∞}, where Q = {p/q : p, q ∈ Z, q = 0} is a set of

rational numbers. As in the case of a standard Cartesian plane, an additional point

∞ is introduced, which is considered to be rational.

So, let us ﬁx as the universal set

U = Q2 ∪ {∞}.

(12.30)





12.2 Elliptic Curves with Rational Points

393

The operation of multiplication of points is deﬁned by the same rule as in the

previous section. Formulate this rule in the form of an algorithm.

**Algorithm of addition of points on the elliptic curve** The sum of the two points

A(x , y ) and B(x , y ) on the elliptic curve

A

A

B

B

2

2

3

` `= {(x, y) ∈ Q : y = x + ax + b} ∪ {O}

(12.31)

is the point C(x , y ), whose coordinates are found by the following rule.

C

C

\1. If A = O, then C = A ⊕ B = B.

\2. If B = O, then C = A ⊕ B = A.

\3. If x = x and y = −y , then C = A ⊕ B = O.

A

B

A

B

\4. In other cases, the parameter  is computed:

⎧

y − y

⎪

B

A ,

A

if

if

\=

\=

⎪

A

A

B,

B,

⎪

⎨x − x

B

` `=

(12.32)

⎪

2

A

⎪3x + a

⎪

⎩

,

2y

A

and the coordinates of the point C will be equal to

2

xC =  − x − x ,

(12.33)

(12.34)

A

B

yC = (x − x ) − y .

A

C

A

Here, the procedure of addition of the points is deﬁned speciﬁcally, since it

does not take the result beyond the extended set of rational numbers. Indeed, all

usual arithmetic operation—addition, subtraction, multiplication and division—are

performed in an algorithm on rational operands, which eventually results in rational

numbers. Division by zero in an algorithm cannot take place due to preliminary

processing of the exceptional case B = −A. Therefore, a theorem similar to

theorem 12.2 occurs.

**Theorem 12.3** The operation of addition of the points deﬁned on the elliptic curve

` `on the set Q

O has the following properties:

2 ∪ { }

\1. A ⊕ O = O ⊕ A = A ∀A ∈ ;

\2. A ⊕ (−A) = O ∀A ∈ ;

\3. A ⊕ B = B ⊕ A ∀A, B ∈ ;

\4. (A ⊕ B) ⊕ C = A ⊕ (B ⊕ C) ∀A, B, C ∈ .

The result of the operation “⊕” belongs to the same extended set of points with

rational coordinates.

As we can see, addition of rational point on an arbitrary elliptic curve has all the

properties of a regular operation of addition of rational numbers.





394

12 Elliptic Curves

**12.3 Implementation of the Addition Algorithm**

Let us consider a software implementation of an algorithm of addition of rational

numbers on an elliptic curve. The program’s input data are the coordinates of the

points A and B; the coordinates of the sum A ⊕ B on the set Q ∪ {O} are entered

2

into the resulting ﬁle.

§

Listing 12.1¤

1 class RationalFraction(object):

2

3

def \_\_init\_\_(self, n, d):

self.n = n

4

self.d = d

5

6

def \_\_eq\_\_(self, other):

return self.n == other.n and \

self.d == other.d

7

8

9

10

11

12

13

def \_\_neg\_\_(self):

return RationalFraction(-self.n, self.d)

14 class RationalPoint(object):

15

16

17

18

19

20

21

22

23

def \_\_init\_\_(self, x, y):

self.x = x

self.y = y

def \_\_eq\_\_(self, other):

return self.x == other.x and \

self.y == other.y

24 # Denominators of coordinates of the point at

infinity

25 # are equated to zero

26 O = RationalPoint(RationalFraction(1, 0), \

27

28

RationalFraction(1, 0))

29 # Parameter a of an elliptic curve

30 a = RationalFraction(-4, 1)

31

32

33 def add(p1, p2):

34

35

if p1.x.d == 0 or p1.y.d == 0:

return p2





12.3 Implementation of the Addition Algorithm

395

36

37

38

39

40

41

42

43

44

45

46

47

48

49

50

51

52

53

54

55

56

57

58

59

60

61

62

63

64

elif p2.x.d == 0 or p2.y.d == 0:

return p1

elif p1.x == p2.x and p1.y == (-p2.y):

return O

else:

k = RationalFraction(0, 0)

c = RationalPoint(RationalFraction(0, 0), \

RationalFraction(0, 0))

if p1 == p2:

k.n = p1.y.d \* \

(3 \* p1.x.n \* p1.x.n \* a.d + \

a.n \* p1.x.d \* p1.x.d)

k.d = 2 \* p1.y.n \* p1.x.d \* \

p1.x.d \* a.d

if k.d < 0:

k.n = -k.n

k.d = -k.d

c.x.n = \

(k.n \* k.n \* p1.x.d \* p2.x.d - \

p1.x.n \* k.d \* k.d \* p2.x.d - \

p2.x.n \* k.d \* k.d \* p1.x.d)

c.x.d = k.d \* k.d \* p1.x.d \* p2.x.d

c.y.n = \

k.n \* p1.y.d \* \

(p1.x.n \* c.x.d - c.x.n \* p1.x.d) -

\

65

66

67

68

69

70

71

72

73

74

75

76

77

78

k.d \* p1.x.d \* c.x.d \* p1.y.n

c.y.d = k.d \* p1.x.d \* c.x.d \* p1.y.d

fraction\_reduce(c.x)

fraction\_reduce(c.y)

if c.x.d < 0:

c.x.n = -c.x.n

c.x.d = -c.x.d

if c.y.d < 0:

c.y.n = -c.y.n

c.y.d = -c.y.d





396

12 Elliptic Curves

79

80

81

82

83

84

85

86

87

88

89

90

91

92

93

94

95

96

97

else:

\# Points are different

k.n = p1.x.d \* p2.x.d \* \

(p2.y.n \* p1.y.d - p1.y.n \* p2.y.d)

k.d = p1.y.d \* p2.y.d \* \

(p2.x.n \* p1.x.d - p1.x.n \* p2.x.d)

if k.d < 0:

k.n = -k.n

k.d = -k.d

c.x.n = \

(k.n \* k.n \* p1.x.d \* p2.x.d - \

p1.x.n \* k.d \* k.d \* p2.x.d - \

p2.x.n \* k.d \* k.d \* p1.x.d)

c.x.d = k.d \* k.d \* p1.x.d \* p2.x.d

c.y.n = k.n \* p1.y.d \* \

(p1.x.n \* c.x.d - c.x.n \* p1.x.d) -

\

98

99

k.d \* p1.x.d \* c.x.d \* p1.y.n

c.y.d = k.d \* p1.x.d \* c.x.d \* p1.y.d

100

101

102

103

104

105

106

107

108

109

110

111

112

113

114

fraction\_reduce(c.x)

fraction\_reduce(c.y)

if c.x.d < 0:

c.x.n = -c.x.n

c.x.d = -c.x.d

if c.y.d < 0:

c.y.n = -c.y.n

c.y.d = -c.y.d

return c

115 def gcd(a, b):

116

117

118

119

120

121

r = 0

\# Euclid’s algorithm

while b != 0:

r = a % b

a = b





12.3 Implementation of the Addition Algorithm

397

122

123

124

125

126

b = r

return a

127 def fraction\_reduce(fraction):

128

129

130

131

132

133

temp = gcd(fraction.n, fraction.d)

fraction.n //= temp

fraction.d //= temp

134 p1 = RationalPoint(RationalFraction(0, 0), \

RationalFraction(0, 0))

136 p2 = RationalPoint(RationalFraction(0, 0), \

135

137

138

RationalFraction(0, 0))

139 with open(’input.txt’) as file:

140

141

142

143

144

145

p1.x.n, p1.x.d, p1.y.n, p1.y.d = \

[int(num) for num in next(file).split()]

p2.x.n, p2.x.d, p2.y.n, p2.y.d = \

[int(num) for num in next(file).split()]

146 result = add(p1, p2)

147

148 with open(’output.txt’, ’w+’) as file:

149

150

151

152

153

output = ’(%d / %d, %d / %d )’ % \

(result.x.n, result.x.d, \

result.y.n, result.y.d)

¦

¥

file.write(output)

For operations with rational fractions, a class RationalFraction is im-

plemented in the program, which consists of two ﬁelds—the numerator and the

denominator of the fraction.

An arbitrary rational point of the plane is characterized by its abscissa and

ordinate. Each of these coordinates is a rational fraction; this is why the de-

scription of the class RationalPoint includes two ﬁelds that store the objects

RationalFraction.

Thus, a rational point of the elliptical curve is represented in the program by a

class containing the objects of other classes.





398

12 Elliptic Curves

For example, the point P (3, −2) of the Cartesian plane can be written in the

1

$

%

3

1

2

1

form

, −

= RationalPoint(RationalFraction(3, 1), and be

represented in the memory of computer as

p1 = {{3, 1}, {−2, 1}}.

The ﬁelds are referred to as follows:

• p1.x.n—numerator of the abscissa of the point P1;

• p1.x.d—denominator of the abscissa of the point P1;

• p1.y.n—numerator of the ordinate of the point P1;

• p1.y.d—denominator of the ordinate of the point P1.

The fraction’s sign will be the sign of its numerator, while in the intermediary

computations the sign of the denominator will be preserved as positive.

We should separately discuss the issue of representing the point at inﬁnity O. In

this implementation, it is introduced as an object

O = RationalPoint(RationalFraction(1, 0), RationalFraction(1,

0))

i.e. the denominators of its coordinates are equated to zero.

The main procedure that executes the addition of the points is called

add() and it operates as follows. In its code, an algorithm presented on page [393](#br401)

is directly reﬂected, and the arithmetic operations on rational fractions are executed

separately for the numerator and for the denominator.

In particular, addition of two fractions is presented in the form:

p1.x.n p2.x.n

p1.x.n p2.x.d + p2.x.n p1.x.d

.

\*

\*

\+

\=

(12.35)

p1.x.d p2.x.d

p1.x.d p2.x.d

\*

Similarly, subtraction, multiplication and division are implemented in the pro-

gram. Such arithmetic operations may result in a reducible fraction. For example,

2

1

the summation

\+

is performed as follows:

3

3

2

3

1

3

2 · 3 + 1 · 3

3 · 3

9

9

\+

\=

\=

.

(12.36)

In this connection, prior to returning the result, the function add() divides the

numerator and the denominator of the fraction by their greatest common divisor,

gcd. For this purpose, an auxiliary function fraction\_reduce() is called.

Computing [of](#br406)[ ](#br406)the greatest [common](#br421)[ ](#br421)divisor of two integers is based on the widely

known Euclid’[s](#br406)[3](#br406)[ ](#br406)algorithm [[32](#br421)[\].](#br421)

3Euclid (Εὐκλείδης) (about 325 BC–before 265 BC), Ancient Greek mathematician.





Problems

399

At the ﬁnal stage, the program outputs a sum of two rational points in the form

( c.x.n / c.x.d, c.y.n / c.y.d )

where c.x.n is the numerator of the abscissa of the result, c.x.d is the

denominator of the abscissa of the result, etc.

**Review Questions**

\1. Deﬁne elliptic curve.

\2. How is the discriminant of the equation of an elliptic curve computed?

\3. Explain how one can, by the sign of the discriminant of the elliptic curve,

establish the number of connected components of its graph.

\4. Enumerate the properties of the point at inﬁnity O.

\5. Explain how the sum of the points A ⊕ B on the elliptic curve is computed.

\6. How can one, knowing the coordinates of some point on the elliptic curve, ﬁnd

the coordinates of the opposite point?

\7. Formulate the necessary and sufﬁcient condition of equality O of the sum of

three points on the elliptic curve.

\8. Deﬁne the sum n of the points on the elliptic curve, where n is an integer.

\9. Enumerate the properties of the operation of addition of points on the elliptic

curve.

**Problems**

**12.1**. Which of the equations listed below specify the elliptic curves on the

expanded Cartesian plane R2 ∪ {O}?

(1) y2 = x2 − x + 1;

(2) y2 = x3 + x + 1;

(3) y2 = x + 1;

(4) y2 = x3;

(5) y2 = x3 + 3x + 2;

(6) y2 = x3 − 3x + 2;

(7) y2 = x3 − 15x/27;

(8) y2 = x4 + x3.

If the curve belongs to the class of elliptical ones, then compute its

discriminant and construct a graph.

**12.2**. Draw a graph of the curve S = {(x, y): y2 = x3 − 12x + 16} and explain

why it does not belong to the class of elliptic curves.

**12.3**. Compute the discriminant for each of the following elliptic curves:

2

3

(1) y = x − 2x + 3;





400

12 Elliptic Curves

2

3

(2) y = x − x − 1;

2

3

(3) y = x + 4x;

2

3

(4) y = x − 10x + 8.

How many connected components does the graph of them contain?

∗**12.4.** Prove that the **duplication formula** for computing of the abscissa of the

point 2A on the curve y2 = x3 + ax + b can be presented in the following

form:

2

3

2

2

A

2y

4

A

2

A

\+ 4

2

3x + a

x − 2ax − 8bx + a

A

x2A

\=

− 2 A =

x

.

(12.37)

3

4

x

ax

\+ 4

b

A

A

A

**12.5**. Verify that the points (−2, 5), (−1, −5) and (103, 1045) belong to the

2

3

elliptic curve y = x − 7x + 19.

**12.6**. Verify that on the curve y2 = x3 + 15 the following equality

2(1, 4) = (−119/64, −1499/512)

is valid.

**12.7**. Compute the following sums of the points on the elliptic curves on the set

Q2:

(1) (−3, 3) ⊕ (1, 3) on the curve y2 = x3 − 7x + 15;

(2) (1, 4) ⊕ (1, 4) on the curve y2 = x3 + x + 14.

**12.8**. Verify the validity of the equalities on the elliptic curve y2 = x3 − 7x +

10:

(1) (5, 10) ⊕ (9, 26) = (2, 2);

(2) (5, 10) ⊕ (2, −2) = (9, −26);

(3) (5, 10) ⊕ (2, 2) = (1/9, 82/27);

(4) (5, −10) ⊕ (1, −2) = (−2, −4).

**12.9**. Compute the sum of the points

(−2, −4) ⊕ (1, 2) ⊕ (2, 2) ⊕ (−3, 2)

on the curve y2 = x3 − 7x + 10.

**12.10**. Perform duplication of the point (5, 12) on the curve y2 = x3 + x + 14.

**12.11**. Compute the sum of the points

(1) 2(7, 19) on the curve y2 = x3 + x + 11;

(2) 3(1, 4) on the curve y2 = x3 + x + 14.





Answers and Solutions

401

∗**12.12.** Compute the sum of the points

2(2, 4) ⊕ 2(33, 190) ⊕ (1, 2)

on the curve y2 = x3 + 5x − 2.

∗**12.13.** Compute the sum of the points

(6, 16) ⊕ (−1, −2) ⊕ (−2)(9, −28)

2

3

on the curve y = x + 5x + 10.

**12.14**. Write a function that checks whether the rational point P (x, y) belongs to

2

3

the elliptic curve y = x + ax + b.

**Answers and Solutions**

[**12.1**](#br407)[** ](#br407)Solution.

Elliptic curve, as is known, is deﬁned by the relation

2

3

y = x + ax + b

for some a, b ∈ R on the condition 4a3 + 27b2 = 0 (see page [383](#br391)). Leaning upon

this deﬁnition, we obtain

(1) y2 = x2 − x + 1 is not an elliptic curve, since the right side lacks the summand

x

3;

(2) y2 = x3 + x + 1 is an elliptic curve; the respective values of the parameters are

a = 1, b = 1, the discriminant is  = −16(4a

3 + 27 2 = −496;

b )

(3) y2 = x + 1 is not an elliptic curve, since it lacks the cubic summand x3;

(4) y2 = x3 is not an elliptic curve, since a = 0, b = 0 and the equality 4a3 +

27b2 = 0 is valid;

(5) y2 = x3 + 3x + 2 satisﬁes the deﬁnition of elliptic curve with the parameters

a = 3 and b = 2, the discriminant is  = −3456;

(6) y2 = x3 −3x+2 is not an elliptic curve, since a = −3, b = 2 and 4a3 +27b2 =

0;

(7) y2 = x3 −5x/27 satisﬁes the deﬁnition of elliptic curve, a = −5/27 and b = 0,

` `= 8000/19683;

(8) the equation y2 = x4 + x3 includes a summand of the fourth degree x4,

therefore, the respective curve does not belong to the class of elliptic curves

(Fig. [12.5](#br410)).





402

12 Elliptic Curves

y

y

a)

b)

x

x

y2 = x3 + x + 1

c)

y2 = x3 + 3x + 2

y

x

y2 = x3 − 15x/27

**Fig. 12.5** Elliptic curves to Problem [**12.1**](#br407). The rectangular mesh on the panels (**a**)–(**c**) has a step

equal to 2

[**12.2**](#br407)[** ](#br407)Solution.

The graph of the curve S is presented in Fig. [12.6](#br411). The curve S is not elliptic,

since the condition of its discriminant’s being other than zero is not valid:  =

−16(4a3 + 27b2) = −16(4(−12)3 + 27 · 162) = 0. The geometric expression of

this fact is the presence on the graph of a self-intersection point with the coordinates

(−2, 0).

[**12.3**](#br407)[** ](#br407)Solution.

Using the formula  = −16(4a3 + 27b2), we obtain

(1)  = −3376, the graph has one connected component;

(2)  = −368, one connected component;

(3)  = −4096, one connected component;

(4)  = 36, 352, the graph consists of two connected components.





Answers and Solutions

403

**Fig. 12.6** The curve S to

Problem [**12.2**](#br407). The

y

rectangular mesh has a step

equal to 2. The point (2, 0) is

an intersection point for the

curve y2 = x3 − 12x + 16

x

y2 = x3 − 12x + 16

[**12.4**](#br408)[** ](#br408)Solution.

2

3

2

3x2 + a

Expanding the expression

A

2y

−2xA and collecting similar summands,

A

we arrive at the formula for x2A

:

2

3

2

9x4 + 6ax2 + a2

\=

\=

\=

\=

A

A

− 2

xA

x2A

2

4y

A

9x4 + 6ax2 + a2 − 8x y2

A

A

A

A

4y2

A

9x4 + 6ax2 + a2 − 8x (x + ax + b)

3

A

A

A

A

A

3

2

4(x + ax + b)

A

A

4

2

A

2

x − 2ax − 8bx + a

.

A

A

3

A

4x + 4ax + 4b

A

In algebraic transformations, the equality y2 = x + ax + b was used, valid for

3

A

A

A

the coordinates of all points of the elliptic curve.

Thus, the algebraic variation of the duplication formula is proved.

[**12.5**](#br408)[** ](#br408)Solution.

Substitute the coordinates of each point into the equation of the curve y2 =

x

3 − 7 + 19:

x

2

3

5 = (−2) − 7(−2) + 19, or 25 = 25;

2

3

(−5) = (−1) − 7(−1) + 19, or 25 = 25;

2

3

1045 = 103 − 7(103) + 19, or 1 092 025 = 1 092 025.





404

12 Elliptic Curves

In all three cases we obtain true equalities, this is why the considered points

belong to the elliptic curve y2 = x3 − 7x + 19.

[**12.6**](#br408)[** ](#br408)Solution.

Use the duplication formula [(](#br397)[12.12](#br397)). Substitute in it the numeric values from the

problem statement a = 0, b = 15, xA = 1 and yA = 4. Then we obtain

⎧


1 −



= −

2

2

⎪

3 · 1

2 + 0

3

8

119

64

⎪

⎨

\=

− 2 · 1 =

− 2 = −

x2A

,

2 · 4



⎪

3

8

119

64

1499

512

⎪

⎩

y2A = −4 +

−

.

Therefore, the equality 2(1, 4) = (−119/64, −1499/512) is valid on the curve

2 = 3 + 15.

y

x

[**12.7**](#br408)[** ](#br408)Answer:

(1) (2, −3);

(2) (−7/4, −21/8).

[**12.9**](#br408)[** ](#br408)Answer: (−2, −4).

[**12.10**](#br408)[** ](#br408)Answer: (1/36, 809/216).

[**12.11**](#br408)[** ](#br408)Answer:

(1) (422/361, 25449/6859);

(2) (793/121, −23132/1331).

[**12.12**](#br409)[** ](#br409)Answer: (33, 190).

[**12.13**](#br409)[** ](#br409)Answer: O.

[**12.14**](#br409)[** ](#br409)Solution.

Let us assume that the rational point P (x, y) is represented in the computing

system memory as the object of a class RationalPoint described in Listing

12.1 (lines 14–21 of the program code).

Let us show the implementation of the function is\_point() that returns the

value True or False depending on the belonging of the point P (x, y) to the

elliptic curve y2 = x3 + ax + b.

def is\_point(p):

\# Point at infinity

if p.x.d == 0 and p.y.d == 0:

return True

elif p.x.d == 0 or p.y.d == 0:

raise ValueError("Zero denomitator of a coordinate")

\# Checking the condition y

y = x

p.x.n

p.x.d

x

x + a

x + b

\*

\*

\*

\*

\*

\*

temp1 = a.d

a.n

b.d

b.d

p.x.n

p.x.n

p.x.n + \

p.x.d + \

\*

\*

\*

\*

\*

\*





Answers and Solutions

405

a.d

temp2 = a.d

b.n

b.d

p.x.d

p.x.d

p.x.d

p.x.d

p.x.d

p.x.d

\*

\*

\*

\*

\*

\*

\*

\*

temp3 = temp2

p.y.n

p.y.n - temp1

p.y.d

p.y.d

\*

\*

\*

\*

return temp3 == 0





**Appendix A**

**Basic Operators in Python and C**

This book uses the Python language to write algorithms [[68](#br422)[,](#br422)[ ](#br422)[71](#br422)[\].](#br422)[ ](#br422)Of course,

when necessary, all the algorithms presented in the text can be rewritten using

any other programming language. In the present Appendix we provide a table of

correspondences between the basic constructs of Python 3 and their analogues in

the C language (see Table [A.1](#br415)).

Both these languages are high-level programming languages, although the l[evel](#br422)

of abstraction in Python is considered to be higher compared to the C language [[50](#br422)[\].](#br422)

As a rule, this results in slower operation of programs in Python.

One of the important differences between the syntaxes of these two languages

consists in that the commands in the C end with a comma, while in Python it is

not necessary to put a semicolon at the end of the command. Another signiﬁcant

difference is associated with marking out a block of operators: C uses braces for

this purpose, while Python uses an indent consisting of exactly four spaces.

A new class in Python can be created as follows:

class Point:

def \_\_init\_\_(self, x, y):

self.x = x

self.y = y

Such a class was used in Chap. [7](#br287)[ ](#br287)for describing a point of the Cartesian plane.

This class contains ﬁelds x and y, representing the coordinates of the point. Also,

this class includes a class constructor that is called when creating an object and is

used for initialization of its ﬁelds. In order to refer to the ﬁelds, the keyword self

can be used, which represents the current class instance automatically transferred as

an argument into each method of this class.

The C la[nguage,](#br421)[ ](#br421)[unl](#br421)[ik](#br421)e Python, is not object-oriented, and C uses structures

instead of classes [[21](#br421)[,](#br421)[ ](#br421)[39](#br421)[\].](#br421)

Let us enumerate some more features of Python reﬂected in the listings of the

programs.

© Springer Nature Switzerland AG 2021

407

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3>





408

A Basic Operators in Python and C

**Table A.1** Correspondences between the basic operators in Python and C

Command or

operation

Python

C

Assignment

x = y

x = y;

Integer variables m, n = 10, -17

int m = 10, n = -17;

Real variables

Logic variables

String variables

Arrays

v = 0.005

w = -1.4

float v = 0.005;

double w = -1.4;

u = True

v = False

u = 1;

v = 0;

s = "String text"

\*

const char s = "String

text";

arr = [1, 2, 3]

arr[2] = 7

int arr[3] = {1, 2, 3};

arr[2] = 7;

Comparison of

variables

x == y

x != y

x == y;

x != y;

Logic operations (not A) and (B or C)

(!A) && (B || C);

(double)m/n

Arithmetic

division

m/n

Integer division

Comments

m//n

m/n

\# comment

// comment

""" Text of multiline

comment """

/\* Text of multiline

comment \*/

Conditional

operator

if a == b:

\# Code1

if (a == b) {

// Code1

elif a == c:

\# Code2

}

else if (a == c) {

else:

// Code2

\# Code3

}

else {

// Code3

}

Ternary operator maxv = a if a>=b else b

maxv = (a>=b) ? a : b;

for loop

for i in range(n):

\# Code

for(int i=0; i<n; i++) {

// Code

}

while loop

Functions

while a == b:

\# Code

while (a == b) {

// Code

}

def sm(a, b):

s = a + b

int sm(int a, int b) {

int s = a + b;

return s

return s;

}

Exchange of

values of two

variables

a, b = b, a

int c = a;

a = b;

b = c;





A

Basic Operators in Python and C

409

In Python, there is a method for generation of lists (including multidimensional

ones):

• creating a list of n numbers ﬁlled with the values from 0 to n - 1:

V = [ i for i in range(n) ]

• creating a two-dimensional list (matrix) ﬁlled with zeroes:

A = [[ 0 for j in range(n) ] \

for i in range(n) ]

Similarly to many other languages, Python provides the means for dealing with

exceptions, which are useful for processing error situations. So, in order to generate

an exception, the keyword raise is used:

raise Exception("Exception message")

In order to process the exception, the construct try-except is used:

try:

a = 5

b = 0

c = a / b

except ZeroDivisionError as e:

print(e)

After executing this code area, the following message will be outputted to the

console:

division by zero





**Appendix B**

**Trigonometric Formulae**

In the formulae of this Appendix, unless otherwise speciﬁed, a, b ∈ R and k, k ∈ Z.

2

2

sin a + cos a = 1;

(B.1)

sin a

cos a

π

tan a =

cot a =

, a = + πk;

(B.2)

2

cos a

sin a

, a = πk;

(B.3)

(B.4)

(B.5)

1

π

1 + tan2 a =

1 + cot2 a =

, a = + πk;

cos2 a

2

1

, a = πk;

sin2 a

2

2

sin 2a = 2 sin a cos a,

cos 2a = cos a − sin a;

(B.6)

(B.7)

2 tan a

π

πk

2

π

tan 2a =

, a =

\+

, a = + πk;

1 − tan2 a

4

2

a

1 − cos a

a

1 + cos a

sin2

\=

,

cos2

\=

;

(B.8)

2

2

2

2

sin(a + b) = sin a cos b + cos a sin b;

sin(a − b) = sin a cos b − cos a sin b;

(B.9)

(B.10)

© Springer Nature Switzerland AG 2021

411

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3>





412

B

Trigonometric Formulae

cos(a + b) = cos a cos b − sin a sin b;

cos(a − b) = cos a cos b + sin a sin b;

(B.11)

(B.12)

tan a + tan b

π

tan(a + b) =

tan(a − b) =

, a, b, a + b = + πk;

(B.13)

(B.14)

1 − tan a tan b

2

tan a − tan b

π

, a, b, a − b = + πk;

1 + tan a tan b

2

$

%

$

$

%

%

a + b

a − b

2

sin a + sin b = 2 sin

sin a − sin b = 2 cos

cos a + cos b = 2 cos

cos a − cos b = −2 sin

cos

sin

;

(B.15)

(B.16)

(B.17)

(B.18)

2

$

%

a + b

2

a − b

;

2

$

%

$

%

a + b

a − b

cos

;

2

2

$

%

$

%

a + b

a − b

sin

;

2

2

sin(a ± b)

cos a cos b

π

tan a ± tan b =

cot a ± cot b =

,

,

a, b = + πk;

(B.19)

(B.20)

2

sin(b ± a)

sin a sin b

a, b = πk;

1

sin a sin b = (cos(a − b) − cos(a + b));

(B.21)

(B.22)

(B.23)

2

1

cos a cos b = (cos(a − b) + cos(a + b));

2

1

sin a cos b = (sin(a − b) + sin(a + b)).

2





**Appendix C**

**The Greek Alphabet**

A, α

B, β

, γ

, δ

E, ε

Z, ζ

alpha

beta

N, ν

, ξ

O, o

, π

P, ρ

nu

xi

gamma

delta

epsilon

zeta

omicron

pi

rho

, σ

T, τ

sigma

tau

H, η

, θ

I, ι

eta

theta

iota

ϒ, υ

` `, ϕ

X, χ

", ψ

, ω

upsilon

phi

K, 

, λ

M, μ

kappa

lambda

mu

chi

psi

omega

© Springer Nature Switzerland AG 2021

413

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3>





**References**

\1. Anderson, J.A.: Discrete Mathematics with Combinatorics, 2nd edn. Prentice Hall (2003)

\2. Arfken, G.B., Weber, H.J.: Mathematical Methods for Physicists, 6th edn. Elsevier Academic

Press, Amsterdam (2005)

\3. Banchoff, T., Wermer, J.: Linear Algebra Through Geometry. Undergraduate Texts in Mathe-

matics, 2nd edn. Springer, Berlin (1992)

\4. Berestetskii, V.B., Lifshitz, E.M., Pitaevskii, L.P.: Quantum Electrodynamics. In: Course of

Theoretical Physics, vol. 4, 2nd edn. Pergamon Press, Oxford (1982)

\5. Bertsekas, D.P., Tsitsiklis, J.N.: Parallel and Distributed Computation: Numerical Methods.

Optimization and Neural Computation; Book 7. Athena Scientiﬁc, Belmont (1997)

\6. Billig, Y.: Quantum Computing for High School Students. Yuly Billig, Ottawa (2018)

\7. Bix, R.: Conics and Cubics: A Concrete Introduction to Algebraic Curves. Undergraduate Texts

in Mathematics, 2nd edn. Springer, Berlin (2006)

\8. Borsuk, K.: Multidimensional Analytic Geometry. Monograﬁe Matematyczne; T. 50. PWN,

Warszawa (1969)

\9. Bretscher, O.: Linear Algebra with Applications, 5th edn. Pearson, London (2013)

\10. Carroll, B.W., Ostlie, D.A.: An Introduction to Modern Astrophysics. Pearson Addison-

Wesley, San Francisco (2007)

\11. Cheney, E.W.: Introduction to Approximation Theory, 2nd edn. American Mathematical

Society, Providence (2000)

\12. Chivers, I., Sleightholme, J.: Introduction to Programming with Fortran, 4th edn. Springer,

Berlin (2018)

\13. Cohen, H.: Number Theory. Graduate Texts in Mathematics; Vol. 239, Vol. I: Tools and

Diophantine Equations. Springer, Berlin (2007)

\14. Cohen, H., Frey, G., Avanzi, R., Doche, C., Lange, T., Nguyen, K., Vercauteren, F.: Handbook

of Elliptic and Hyperelliptic Curve Cryptography. Discrete Mathematics and Its Applications.

Chapman & Hall/CRC, Boca Raton (2006)

\15. Cohn, P.M.: Algebra : Volume 1, 2nd edn. Wiley, Chichester (1982)

\16. Cormen, T.H., Leiserson, C.E., Rivest, R.L., Stein, C.: Introduction to Algorithms, 3rd edn.

The MIT Press, Cambridge (2009)

\17. Courant, R., Robbins, H.: What is Mathematics? An Elementary Approach to Ideas and

Methods, 2nd edn. Oxford University Press, New York (1996)

\18. Cover, T.M., Thomas, J.A.: Elements of Information Theory, 2nd edn. Wiley, New York (2006)

\19. Coxeter, H.S.M.: Introduction to Geometry, 2nd edn. Wiley, New York (1969)

© Springer Nature Switzerland AG 2021

415

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3>





416

References

\20. D’Alberto, P., Nicolau, A.: Adaptive Strassen’s matrix multiplication. In: Proceedings of

the 21st Annual International Conference on Supercomputing, ICS’07, June 18–20, Seattle,

Washington, pp. 284–292. ACM, New York (2007)

\21. Deitel, P.J., Deitel, H.: C for Programmers with an Introduction to C11. Deitel Developer

Series. Pearson Education, London (2013)

\22. Diestel, R.: Graph Theory. Graduate Texts in Mathematics, vol. 173, 5th edn. Springer, Berlin

(2017)

\23. Dubrovin, B.A., Fomenko, A.T., Novikov, S.P.: Modern Geometry — Methods and Applica-

tions. Part I. The Geometry of Surfaces, Transformation Groups, and Fields. Graduate Texts in

Mathematics, vol. 93, 2nd edn. Springer, Berlin (1992)

\24. Gamelin, T.W.: Complex Analysis. Undergraduate Texts in Mathematics. Springer, Berlin

(2001)

\25. Gantmacher, F.R.: The Theory of Matrices, vol. 1. American Mathematical Society, Providence

(2000)

\26. Gantmacher, F.R.: The Theory of Matrices, vol. 2. American Mathematical Society, Providence

(2000)

\27. Golub, G.H., Loan, C.F.V.: Matrix Computations, 4th edn. The Johns Hopkins University Press,

Baltimore (2013)

\28. Graham, R.L., Knuth, D.E., Patashnik, O.: Concrete Mathematics: A Foundation for Computer

Science, 2nd edn. Addison-Wesley, Reading (1994)

\29. Haggarty, R.: Discrete Mathematics for Computing. Addison-Wesley, Reading (2002)

\30. Halmos, P.R.: Finite-Dimensional Vector Spaces. Undergraduate Texts in Mathematics.

Springer, Berlin (1993)

\31. Harary, F.: Graph Theory. Addison-Wesley, Reading (1969)

\32. Hardy, G.H., Wright, E.M.: An Introduction to the Theory of Numbers, 6th edn. Oxford

University Press, Oxford (2008)

\33. Hazewinkel, M. (ed.): Encyclopaedia of Mathematics, 10 volume-set. Springer, Berlin (1994)

\34. Higham, N.J.: Functions of Matrices: Theory and Computation. SIAM, Philadelphia (2008)

\35. Hungerford, T.W.: Algebra. Graduate Texts in Mathematics, vol. 73. Springer, New York

(2011)

\36. Il’in, V.A., Poznyak, E.G.: Linear Algebra. Collets (1986)

\37. Ito, K.: Encyclopedic Dictionary of Mathematics, 2nd edn. The MIT Press; Mathematical

Society of Japan, Massachusetts Institute of Technology (1987)

\38. Jeffrey, A., Dai, H.H.: Handbook of Mathematical Formulas and Integrals, 4th edn. Academic

Press, Cambridge (2008)

\39. Kernighan, B.W., Ritchie, D.M.: The C Programming Language, 3rd edn. Prentice Hall,

Englewood Cliffs (1988)

\40. Knuth, D.E.: The Art of Computer Programming. Fundamental Algorithms, vol. 1, 3rd edn.

Addison-Wesley, Reading (1997)

\41. Kurgalin, S., Borzunov, S.: The Discrete Math Workbook: A Companion Manual for Practical

Study. Texts in Computer Science. Springer, Berlin (2018)

\42. Kurgalin, S., Borzunov, S.: A Practical Approach to High-Performance Computing. Springer,

Berlin (2019)

\43. Kurosh, A.: Higher Algebra, 4th edn. Mir Publishers, Moscow (1984)

\44. Landau, L.D., Lifshitz, E.M.: Quantum Mechanics: Non-relativistic Theory. Course of Theo-

retical Physics, vol. 3, 3rd edn. Pergamon Press, Oxford (1989)

\45. Landau, L.D., Lifshitz, E.M.: The Classical Theory of Fields. Course of Theoretical Physics,

vol. 2, 4th edn. Butterworth-Heinemann, Oxford (1996)

\46. Langtangen, H.P.: A Primer on Scientiﬁc Programming with Python. Texts in Computational

Science and Engineering, vol. 6, 4th edn. Springer, Berlin (2014)

\47. Magnus, J.R., Neudecker, H.: Matrix Differential Calculus with Applications in Statistics and

Econometrics. Wiley Series in Probability and Statistics, 3rd edn. Wiley, New York (2019)

\48. Markov, A.A.: The theory of algorithms (in Russian). Trudy Mat. Inst. Steklov **42**, 3–375

(1954)





References

417

\49. Markov, A.A., Nagorny, N.M.: The Theory of Algorithms. Mathematics and its Applications,

vol. 23. Springer, Netherlands (1988)

\50. Martelli, A., Ravenscroft, A., Holden, S.: Python in a Nutshell, 3rd edn. O’Reilly, Beijing

(2017)

\51. McConnell, J.J.: Analysis of Algorithms: An Active Learning Approach, 2nd edn. Jones and

Bartlett Publishers, Burlington (2008)

\52. Miller, R., Boxer, L.: Algorithms Sequential and Parallel: A Uniﬁed Approach, 3rd edn.

Cengage Learning, Boston (2013)

\53. Mirsky, L.: An Introduction to Linear Algebra. Clarendon Press, Oxford (1955)

\54. Nielsen, M.A., Chuang, I.L.: Quantum Computation and Quantum Information, 10th anniver-

sary edn. Cambridge University Press (2010)

\55. Ore, O.: Theory of Graphs. Colloquium Publications; vol. 38. American Mathematical Society,

Providence (1962)

\56. Ortega, J.M.: Introduction to Parallel and Vector Solution of Linear Systems. Frontiers in

Computer Science. Springer, Berlin (1988)

\57. Pérez, F., Granger, B.E.: IPython: a system for interactive scientiﬁc computing. Comput. Sci.

Eng. **9**(3), 21–29 (2007)

\58. Press, W.H., Teukolsky, S.A., Vetterling, W.T., Flannery, B.P.: Numerical Recipes: The Art of

Scientiﬁc Computing, 3rd edn. Cambridge University Press, Cambridge (2007)

\59. Rosen, K.H.: Discrete Mathematics and Its Applications, 7th edn. McGraw-Hill, New York

(2012)

\60. Rosen, K.H., Michaels, J.G., Gross, J.L. et al. (eds.): Handbook of Discrete and Combinatorial

Mathematics. Discrete Mathematics and Its Applications. CRC Press, Boca Raton (2000)

\61. Sedgewick, R.: Algorithms in C. Part 5. Graph Algorithms, 3rd edn. Addison-Wesley, Boston

(2001)

\62. Sedgewick, R., Wayne, K., Dondero, R.: Introduction to Programming in Python: An Interdis-

ciplinary Approach. Addison-Wesley Professional, Princeton University, Princeton (2015)

\63. Shafarevich, I.R.: Algebra I: Basic Notions of Algebra. Encyclopaedia of Mathematical

Sciences, vol. 11. Springer, Berlin (2005)

\64. Shafarevich, I.R., Remizov, A.O.: Linear Algebra and Geometry, 3rd edn. Springer, Berlin

(2013)

\65. Shilov, G.E.: An Introduction to the Theory of Linear Spaces. Martino Fine Books, Eastford

(2013)

\66. Sominskii, I.S.: The Method of Mathematical Induction. Popular Lectures in Mathematics, vol.

\1. Blaisdell Publishing Company, New York (1961)

\67. Steane, A.: Quantum computing. Rep. Progress Phys. **61**, 117–173 (1998)

\68. The Python Tutorial (2019). <https://docs.python.org/3/tutorial/index.html>

\69. Trahtenbrot, B.A.: Algorithms and Automatic Computing Machines. Topics in Mathematics.

D. C. Heath and Company, Boston (1963)

\70. Vorobiev, N.N.: Fibonacci Numbers. Popular Lectures in Mathematics, vol. 2. Springer, Basel

AG (2002)

\71. Welcome to Python.org (2019). <https://www.python.org/>

\72. Williams, C.P.: Explorations in Quantum Computing. Texts in Computer Science, 2nd edn.

Springer, Berlin (2011)

\73. Wilson, R.J.: Introduction to Graph Theory, 4th edn. Longman, Harlow (1998)

\74. Wirth, N.: Pascal and Its Successors. Springer, Berlin (2002)

\75. Zapryagaev, S.A.: Introduction to Quantum Information Systems [in Russian]. Voronezh State

University Textbooks. VSU Publishing, Voronezh (2015)

\76. Zorich, V.A.: Mathematical Analysis I. Universitext, 2nd edn. Springer, Berlin (2015)





**Index**

**Numbers**

(0, 1)-matrix, see Matrix, binary

Angle between planes, [312](#br321)

Annihilating polynomial, see Polynomial,

annihilating

Anomaly of eccentricity, [360](#br369)

Anti-Hermitian matrix, see Matrix, anti-

Hermitian

**A**

Abel–Rufﬁni theorem, see Theorem,

Abel–Rufﬁni

Applicate, [256](#br267)

Abscissa, [256](#br267)

Argand diagram, [174](#br186)

Algebraic complement, see Cofactor

Algebraic form of a complex number, see

Complex number, algebraic form

Algorithm, [12](#br27)

Argument of a complex number, [175](#br187)

principal value, [175](#br187)

Array, [15](#br30)

two-dimensional, [15](#br30)

of addition of points on the elliptic curve,

[393](#br401)

computing the determinant, [68](#br82)

Euclid’s, [398](#br406)

Gram–Schmidt (see Gram–Schmidt

process)

Associativity of addition, [6](#br21)

Associativity of multiplication, [8](#br23)

Asymptotes to a hyperbola, [361](#br370)

Asymptotic complexity, [14](#br29), [184](#br196)

of Gaussian elimination, [137](#br150)

properties, [12](#br27)

determinateness, [12](#br27)

directedness, [12](#br27)

discreteness, [12](#br27)

elementary character of steps, [12](#br27)

mass character, [12](#br27)

**B**

Backward pass, [137](#br150)

Basic minor, see Minor, basic

Basic minor theorem, see Theorem, basic

minor

Roy–Warshall (see Algorithm, Warshall)

Strassen, [11](#br26)

Warshall, [18](#br33), [20](#br35), [29](#br44)

modiﬁed, [29](#br44)

Basic operations, [13](#br28), [14](#br29)

Basis expansion of a vector, [257](#br268)

Basis states, [184](#br196)

Basis step, [53](#br67)

Alphabet

Big O notation, [14](#br29)

Bilinear form, [335](#br344)

polar, [338](#br347)

Greek, [413](#br419)

Latin, [1](#br16)

Altitude of a triangle, [291](#br301)

Angle between a line and a plane, [325](#br334)

Angle between lines, [281](#br291), [323](#br332)

adjacent, [281](#br291)

positively deﬁnite, [336](#br345)

properties of linearity, [335](#br344)

symmetric, [336](#br345)

Bisector of a triangle, [291](#br301)

© Springer Nature Switzerland AG 2021

419

S. Kurgalin, S. Borzunov, Algebra and Geometry with Python,

<https://doi.org/10.1007/978-3-030-61541-3>





420

Index

Bit, [183](#br195)

Condition of intersection of lines, [326](#br335)

Block matrix, [186](#br198)

Bordering minor method, see Method,

bordering minor

Condition of line’s belonging to the plane, [325](#br334)

Condition of orthogonality of planes, [312](#br321)

Condition of parallelism of a line and a plane,

[325](#br334)

Branch of a hyperbola, [361](#br370), [369](#br378)

Condition of parallelism of planes, [312](#br321)

Condition of parallelism of two lines, [326](#br335)

Condition of perpendicularity of a line and a

plane, [325](#br334)

Conjugate of the complex number, [174](#br186)

Conjunction, [20](#br35), [21](#br36)

**C**

Canonical equation of a line, [321](#br330)

Canonical form of a quadratic form, [339](#br348)

Canonical form of equation, [178](#br190)

Canonical form of the equation of curve of the

second order, [357](#br366)

Constant term, [357](#br366)

Controlled NOT, [189](#br201)

Canonical system of coordinates, see

Coordinate system, canonical

Cardinality, [19](#br34)

Controlled phase element, [189](#br201)

Coordinates of a vector, [217](#br228)

Coordinate system

Cauchy–Bunyakovsky inequality, see

Inequality, Cauchy–Bunyakovsky

Cauchy–Schwarz inequality, see Inequality,

Cauchy–Bunyakovsky

Cayley–Hamilton theorem, see Theorem,

Cayley–Hamilton

canonical, [357](#br366)

Cartesian, [174](#br186), [256](#br267), [277](#br287)

polar, [174](#br186)

Coplanar vectors, [264](#br275), [311](#br320)

Corner minor, see Minor, corner

C, programming language, [2](#br17), [15](#br30)

Cramer’s rule, see Method, Cramer

Cross-diagonal, see Secondary diagonal

Cross product, see Vector product

Cryptography, [384](#br392)

Central curves, [362](#br371)

Characteristic equation, [226](#br237)

Characteristic polynomial, see Polynomial,

characteristic

Circle, [357](#br366)

class O(g(n)), [14](#br29)

Curves of the second order, [357](#br366)

degenerate, [363](#br372)

Coefﬁcients of a linear combination, [61](#br75)

Coefﬁcients of a system, [123](#br136)

Coefﬁcients of the straight line equation, [278](#br288)

Cofactor, [46](#br60)

non-degenerate, [363](#br372)

Cusp, [384](#br392)

Collinearity, [223](#br234)

**D**

Collinear vectors, [255](#br266)

Column of a matrix, [1](#br16)

Degree of polynomial, [178](#br190)

Determinant, [43](#br57)

Columns

of the ﬁrst order, [45](#br59)

linearly dependent, [61](#br75)

Laplace expansion, [47](#br61)

linearly independent, [61](#br75)

Commutativity of addition, [6](#br21)

Commutator, [9](#br24)

Complementary minor of the element, [46](#br60)

Complex number, [173](#br185)[–](#br190)[178](#br190)

algebraic form, [174](#br186)

of the n-th order, [45](#br59), [46](#br60)

of the second order, [43](#br57)

of the third order, [43](#br57), [44](#br58)

Vandermonde, [67](#br81)

Determinant of a system of vectors, [221](#br232)

Deviation of a point from a plane, [313](#br322)

Deviation of a point from line, [285](#br295)

Diagonalization of a matrix, [230](#br241)

Diagonal matrix, see Matrix, square, diagonal

Difference of matrices, [6](#br21)

Difference of vectors, [218](#br229)

Digraph, see Graph, directed

Dirac matrices, [185](#br197), [186](#br198)

Dirac notation, [183](#br195)

exponential form, [176](#br188)

imaginary part, [173](#br185)

purely imaginary, [174](#br186)

real part, [173](#br185)

trigonometric form, [174](#br186), [175](#br187)

Components of a vector, [217](#br228)

Composition of operators, [187](#br199)

Computational basis states, [184](#br196)

Condition of belonging of lines to the same

plane, [326](#br335)

Directing vector, see Vector, directing

Direction cosines, [310](#br319)





Index

421

Directrix

**F**

of an ellipse, [358](#br367)

of a hyperbola, [361](#br370)

of a parabola, [362](#br371)

Fermat last theorem, see Theorem, Fermat last

Focal distance of an ellipse, [358](#br367)

Focal parameter of a parabola, [362](#br371)

Focus

Disjunction, [21](#br36)

Distance between the points, [259](#br270)

Distance from a point to a plane, [313](#br322)

Distributivity of multiplication with respect to

addition, [8](#br23)

of an ellipse, [357](#br366)

of a hyperbola, [361](#br370)

of a parabola, [362](#br371)

Formula

Dot product, see Scalar product

Duplication formula, see Formula, of

duplication

Cardano, [179](#br191)

de Moivre’s, [176](#br188), [195](#br207)

of duplication, [400](#br408)

Duplication of a point, [388](#br396)

Euler’s for complex numbers, [176](#br188)

matrix product inversion, [71](#br85)

Fortran, programming language, [15](#br30)

Forward pass, [136](#br149)

**E**

Eccentricity

Free unknown, [138](#br151)

of a hyperbola, [361](#br370)

Function

Eccentricity of an ellipse, [358](#br367)

Echelon matrix, see Matrix, echelon

Edge, [19](#br34)

exponential, [176](#br188)

fractionally rational, [57](#br71)

time-complexity, [14](#br29)

Eigenvalue, [226](#br237)

trigonometric, [176](#br188)

Eigenvector, [226](#br237)

Element π/8, [188](#br200)

Elementary transformations, [49](#br63), [61](#br75), [129](#br142)

Elements of a matrix, [1](#br16)

Fundamental system of solutions, [138](#br151), [139](#br152)

Fundamental theorem of algebra, see Theorem,

fundamental of algebra

Ellipse, [357](#br366)

Elliptic curve, [383](#br391)

**G**

Endpoints, [19](#br34)

Gate, [184](#br196), [187](#br199)

Endpoints of a segment, [287](#br297)

Equal complex numbers, [173](#br185)

Equality of matrices, [4](#br19)

Gaussian elimination, see Method, Gauss

General equation of a plane, [308](#br317)

complete, [308](#br317)

Equal vectors, [217](#br228), [255](#br266)

incomplete, [308](#br317)

Equation of a line that passes through the two

points, [323](#br332)

General equation of a straight line on a plane,

[278](#br288)

Equation of a plane that is orthogonal to the

vector, [307](#br316)

Gram–Schmidt process, [224](#br235)

Graph, [19](#br34)

Equation of a plane that passes through the

three points, [312](#br321)

directed, [18](#br33), [19](#br34), [29](#br44)

undirected, [19](#br34)

Equation of a straight line through two given

points, [280](#br290)

Graph diagram, [19](#br34)

Graph theory, [19](#br34)

Equation of curve of the second order, [357](#br366)

Euclidean space, [224](#br235)

Euclid’s algorithm, see Algorithm, Euclid’s

Euler’s formula, see Formula, Euler’s for

complex numbers

**H**

Hadamard element, [188](#br200)

Hadamard gate, [188](#br200)

Euler’s identity for Pauli matrices, [200](#br212)

Evolution of the quantum system, [184](#br196)

Expansion of the vector in the basis, [222](#br233)

Exponential form of a complex number, see

Complex number, exponential form

Exponent of a matrix, [57](#br71)

Hermitian conjugate matrix, see Matrix,

Hermitian conjugate

Hermitian matrix, see Matrix, Hermitian

Hesse normal form, see Normal form of the

equation of the line

High-performance computing, [11](#br26)





422

Index

Hoare triple, [13](#br28)

Hyperbola, [360](#br369)

equilateral, [369](#br378)

**M**

Magnitude of a vector, [255](#br266)

Main diagonal, [3](#br18)

Matrix, [1](#br16)

adjacency, [19](#br34)

adjugate, [50](#br64)

**I**

Identity permutation, see Permutation, identity

Identity transformation, [188](#br200)

Imaginary part of a complex number, see

Complex number, imaginary part

Imaginary unit, [173](#br185)

Incident vertex and edge, [19](#br34)

Incomplete gamma function, [69](#br83)

Inductive step, [53](#br67)

anti-Hermitian, [198](#br210)

of bilinear form, [335](#br344)

binary, [5](#br20)

brief record, [1](#br16)

classical adjoint (see Matrix, adjugate)

cofactor, [50](#br64)

complex, [2](#br17)

echelon, [61](#br75)

Inequality

functional, [11](#br26)

Cauchy–Bunyakovsky, [232](#br243)

triangle (see Triangle inequality)

Inner product, see Scalar product

Intercept form of the equation of a plane, [309](#br318)

Intercept form of the equation of a straight line,

[283](#br293)

Hermitian, [181](#br193)

Hermitian conjugate, [180](#br192)

Hilbert, [71](#br85)

inverse, [50](#br64), [126](#br139)

lower triangular, [4](#br19), [51](#br65)

notations, [2](#br17)

Inversion, [45](#br59), [65](#br79)

of quadratic form, [337](#br346)

reachability, [20](#br35), [29](#br44)

real, [2](#br17)

**J**

rectangular, [2](#br17)

Jacobi identity

self-adjoint (see Matrix, Hermitian)

square, [2](#br17)

for commutators, [10](#br25)

for vectors, [265](#br276)

antisymmetric, [4](#br19)

Jacobi method, see Method, Jacobi

Java, programming language, [15](#br30)

degenerate (see Matrix, square,

singular)

diagonal, [3](#br18), [52](#br66)

identity, [3](#br18), [50](#br64)

nondegenerate (see Matrix, square,

nonsingular)

**K**

Known terms, [123](#br136)

Kronecker–Capelli theorem, see Theorem,

Kronecker–Capelli

Kronecker symbol, [4](#br19)

nonsingular, [50](#br64)

null (see Matrix, square, zero)

singular, [50](#br64)

symmetric, [4](#br19)

unit (see Matrix, square, identity)

zero, [3](#br18)

transposed, [3](#br18), [4](#br19)

**L**

Lagrange’s identity, [195](#br207), [265](#br276)

Lagrange’s method, see Method, Lagrange’s

Laplace expansion, [47](#br61)

unitary, [182](#br194)

upper triangular, [4](#br19), [51](#br65)

Matrix algebra, [5](#br20)

Law of inertia, [344](#br353)

Length of a vector, [224](#br235)

Matrix form of a system, [124](#br137)

Matrix of a system, [124](#br137)

augmented, [124](#br137), [129](#br142)

Matrix of a system of vectors, [221](#br232)

Matrix power theorem, see Theorem, matrix

power

Linear combination of rows, [61](#br75)

Linear combination of vectors, [218](#br229)

Linearly dependent system of vectors, [219](#br230)

Linearly independent system of vectors, [218](#br229)

Linear term, [357](#br366)

List, [15](#br30)

Matrix, skew-Hermitian, see Matrix,

anti-Hermitian

Measurement of state, [184](#br196)

Median of a triangle, [291](#br301)

Logarithm of a matrix, [58](#br72)

Lower triangular matrix, see Matrix, lower

triangular





Index

423

Parameter of a parabola, see Focal parameter

Method

bordering minor, [64](#br78)

Cramer, [125](#br138)

elementary transformations, [61](#br75)

of elimination of unknowns (see Method,

Gauss)

of a parabola

Parameter of a segment, [287](#br297)

Parametric equation of a line, [321](#br330)

Parametric form of an ellipse, [359](#br368)

Pascal, programming language, [15](#br30)

Path, [19](#br34)

Gauss, [129](#br142)

Gauss–Jordan, [150](#br163)

trivial, [19](#br34)

of an inverse matrix, [126](#br139)

Jacobi, [343](#br352)

Pauli element, [188](#br200)

Pauli matrices, [185](#br197)

Lagrange’s, [340](#br349)

Pencil of planes, [313](#br322)

mathematical induction, [21](#br36), [53](#br67), [195](#br207)

Minkowski inequality, see Triangle inequality

Minor, [59](#br73)

Permutation, [45](#br59), [65](#br79)

identity, [45](#br59)

Phase element, [188](#br200)

basic, [60](#br74)

Pivot element, [136](#br149)

corner, [343](#br352)

Pivot row, [61](#br75)

Mixed product, see Scalar triple product

Modulus of a complex number, [175](#br187)

Modulus of a vector, [255](#br266)

Plane, [277](#br287)

complex, [174](#br186)

Point at inﬁnity, [384](#br392)

Polynomial, [45](#br59), [56](#br70), [178](#br190)

annihilating, [230](#br241)

**N**

characteristic, [227](#br238)

of a matrix, [56](#br70)

Position vector, [174](#br186), [176](#br188), [256](#br267)

Postcondition, [13](#br28)

Precondition, [13](#br28)

n-dimensional space, [218](#br229)

Normal, see Normal vector

Normal equation of a plane, [310](#br319)

Normal form of the equation of the line, [284](#br294)

Normalized vector, [220](#br231), [255](#br266), [257](#br268)

Normalizing factor, [285](#br295)

Normal vector, [278](#br288)

Norm of a vector, [224](#br235)

properties, [224](#br235)

Predicate, [53](#br67)

Principle of mathematical induction, see

Method, mathematical induction

Product of a number and a matrix, [6](#br21)

Product of a number and a vector, [217](#br228)

Product of complex numbers, [173](#br185)

Product of matrices, [7](#br22)

Projection of a point on the line, [256](#br267)

Projection of a vector on the line, [256](#br267)

Projection on |0
` `and |1
, [188](#br200)

Proof of the algorithm correctness, [12](#br27)

Properties of determinants, [48](#br62)

Property of identity matrix, [8](#br23)

Property of zero matrix, [8](#br23)

Pythagorean theorem, see Theorem,

Pythagorean

Null vector, see Zero vector

Numbers

complex, [173](#br185)

ratio, [192](#br204)

Fibonacci, [67](#br81)

Number theory, [384](#br392)

NumPy, library, [18](#br33)

n-vector, see Vector

**O**

Opposite point, [386](#br394)

Opposite vector, [218](#br229)

Optical property

of an ellipse, [359](#br368)

of hyperbola, [361](#br370)

of a parabola, [363](#br372)

Ordinate, [256](#br267)

Python, programming language, [2](#br17), [15](#br30), [68](#br82), [71](#br85),

[135](#br148)

**Q**

Quadratic form, [337](#br346)

alternating, [344](#br353)

Orthogonality, [223](#br234), [224](#br235), [258](#br269)

Orthonormality, [224](#br235)

degenerate, [338](#br347)

negatively deﬁnite, [344](#br353)

nondegenerate, [338](#br347)

positively deﬁnite, [344](#br353)

Quadratic term, [357](#br366)

**P**

Parallelepiped, [263](#br274), [264](#br275)

Parameter of a line, [321](#br330)





424

Index

Quantum computer, [183](#br195)

Quantum-mechanical operator, [186](#br198)

Quantum system, [183](#br195)

Qubit, [183](#br195)

Skew-Hermitian matrix, see Matrix,

anti-Hermitian

Skew lines, [326](#br335)

Slope-intercept form of the equation of a

straight line, [277](#br287)

Slope-intercept form of the equation of a

straight line passing through the

given point, [279](#br289)

**R**

Rank, [60](#br74), [135](#br148)

Rank of a quadratic form, [338](#br347), [343](#br352)

Real part of a complex number, see Complex

number, real part

Slope of a straight line, [277](#br287)

Solution of the system of equations, [123](#br136)

trivial, [138](#br151)

Right-hand side of equations, see Known terms Space

Root n-dimensional, [218](#br229)

of equation, [178](#br190)

one-dimensional, [218](#br229)

three-dimensional, [218](#br229)

two-dimensional, [218](#br229)

Spur, see Trace

Strassen algorithm, see Algorithm, Strassen

Sum of complex numbers, [173](#br185)

Sum of matrices, [5](#br20)

n-th of complex number, [176](#br188)

of unit, [177](#br189), [194](#br206), [195](#br207)

Rouché–Capelli theorem, see Theorem,

Kronecker–Capelli

Route, [19](#br34)

Row of a matrix, [1](#br16)

Rows

Sum of vectors, [217](#br228), [255](#br266)

Sylvester’s criterion, [344](#br353)

System of linear equations, [123](#br136)

consistent, [123](#br136)

linearly dependent, [61](#br75)

linearly independent, [61](#br75)

Roy–Warshall algorithm, see Algorithm,

Warshall

determined, [123](#br136), [125](#br138)

homogeneous, [123](#br136), [140](#br153), [226](#br237)

inconsistent, [123](#br136)

**S**

non-homogeneous, [123](#br136)

rectangular, [123](#br136)

Scalar, [1](#br16)

Scalar product, [223](#br234)

properties, [223](#br234)

square, [123](#br136), [124](#br137)

undetermined, [123](#br136)

Scalar triple product, [263](#br274)

properties, [263](#br274)

Secondary diagonal, [3](#br18)

Secular equation, [230](#br241)

Secular motion, [230](#br241)

Segment, [287](#br297)

Self-adjoint matrix, see Matrix, Hermitian

Self-intersection, [384](#br392)

Semiaxis

**T**

Tangent, [359](#br368), [365](#br374)

to an ellipse, [359](#br368)

to a hyperbola, [361](#br370)

to a parabola, [363](#br372)

Tetrahedron, [264](#br275)[,](#br275)[ ](#br275)[315](#br324)

Theorem

ellipse

Abel–Rufﬁni, [178](#br190)

basic minor, [61](#br75)

major, [357](#br366)

hyperbola

Cayley–Hamilton, [230](#br241)

Fermat last, [384](#br392)

imaginary, [360](#br369)

real, [360](#br369)

Sequence

Fibonacci (see Numbers, Fibonacci)

Series, [57](#br71)

fundamental of algebra, [178](#br190)

Kronecker–Capelli, [129](#br142), [220](#br231)

Laplace, [47](#br61)

matrix power, [56](#br70)

Set

Pythagorean, [233](#br244)

Rouché–Capelli (see Theorem, Kronecker–

Capelli)

of complex numbers, [173](#br185)

of real numbers, [173](#br185)

Signature of a quadratic form, [344](#br353)

Similarity transformation, [225](#br236)

Similar matrices, [225](#br236)

Time-complexity function, see Function,

time-complexity

Trace, [11](#br26), [31](#br46)





Index

of the unit matrix, [11](#br26)

425

directing, [321](#br330)

Transposition, [48](#br62)

Triangle inequality, [193](#br205), [224](#br235)

Triangle rule, [44](#br58)

Vector equation of a plane, [307](#br316)

Vector product, [260](#br271)

properties, [260](#br271)

Trigonometric form of a complex number, see

Complex number, trigonometric

form

Vector triple product, [265](#br276)

Vertex, [19](#br34)

of an ellipse, [357](#br366)

Trigonometric formulae, [411](#br417)

of a hyperbola, [361](#br370)

of a parabola, [362](#br371)

Viète formulae, [195](#br207)

**U**

Unitary matrix, see Matrix, unitary

Unit vector, [255](#br266)

**W**

Upper triangular matrix, see Matrix, upper

triangular

Warshall algorithm, see Algorithm, Warshall

**Z**

**V**

Zero equation, [129](#br142)

Vector, [1](#br16), [217](#br228), [255](#br266)

Zero vector, [218](#br229), [220](#br231), [255](#br266)


