# The Bugs We Left Behind: Evaluating Autonomous Fuzzing Infrastructures for Overlooked Bugs and Vulnerabilities


## Abstract

In a world that relies on digital systems, the security of software applications is a crucial property to protect both people and their assets from cyberattacks. To this end, numerous techniques have been proposed that can detect a wide range of vulnerabilities before they can be exploited by malicious entities.
One of the most prominent example is *Fuzz Testing*, a technique that works by repeatedly running the tested software, generating new inputs each time to exercise as many functionalities of the code as possible: the key idea is that by generating different inputs, the fuzzer will eventually produce one that is capable of triggering a bug.
Thanks to their fuzzing strategies, fuzzers shine in producing inputs that allow them to execute new code as testing time passes: however, in their pursuit of constantly increasing coverage, fuzzers may miss bugs that do not cause observable behaviors at a high level. To tackle this issue, fuzzing is often used in combination with software sanitizations,
a technique that detects specific silent bugs at run-time, and the combination of the two techniques has become the most popular approach to detecting bugs in software.
To ease the deployment of fuzzing, fuzzing frameworks are being proposed. While they usually rely on a private disclosure mechanism for new bugs, these frameworks publicly release lots of data that can be analyzed: with all this accessible data, no
bug should be overlooked, or an attacker could leverage the available data to detect it with a much lower effort than running fuzzing campaigns, and potentially exploit it to attack the target software.
In this thesis, we are going to evaluate fuzzing frameworks for possibly overlooked bugs. by exploring two main directions: first, we are going to evaluate fully autonomous mechanisms, where suboptimal configurations or procedures may cause some bugs to be missed; then, we are going to evaluate another class of frameworks where the human factor is crucial in the detection of new bugs and vulnerabilities. 
We will show that, unfortunately, these frameworks do indeed miss a relevant number of bugs, that can be detected with little effort using publicly available data, and some of them have security implications. 
After reporting all the bugs, we identify the fundamental issues that cause these frameworks to miss bugs and propose enhancements to allow them to detect bugs and vulnerabilities more accurately.
