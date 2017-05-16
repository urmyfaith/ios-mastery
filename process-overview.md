
# Process Overview

This article lists the steps of iOS app development process, giving your a bird view on what has been done and paid attention. Each step has the blur corners on intersected scopes, which is the nature of real life that the rigid minded engineer has to learn coping with.

* 1. Requirement Analysis
* 2. Software [Architecting](2-architecting). I would avoid the word "design" here, since that may mean different jobs and products for different people, such as "product design", "UI design", or "Software High/Low Level Design" that is what i refer as software architecting here. One key goals among many is to clearly separate the problem/feature and locate the code (classes) to address the problems.
  * 2.2 Software Analysis
* 3. [Coding](3-coding), generally speaking.
  * 3.1 Xcode project creation, Target info (such as entitlements) and Info.plist modification.
  * 3.2 non-coding. Such as the editing in Interface Builder, CoreData model, and AssetCatalog, just name few.
  * 3.3 coding, with a programming languages. Here only using Swift.
* 4. [Compiling](4-compiling)
  * 4.1 Compiler setting, such as syntax warnings, and code generation optimization
  * 4.2 Code Signing
  * 4.3 LLVM
* 5. Testing (in [quality/correctness](quality/correctness))
  * 5.1 Unit Test and XCTest
  * 5.2 UI Test
* 6. Debugging (in [quality/debugging](quality/debugging))
  * 6.1 LLDB
  * 6.2 Tips
* 7. Performance Profiling (in [quality/performance](quality/performance))
  * 7.1 Performance Overview
  * 7.2 Instruments
* 8. Releasing
  * 8.1 Ad Hoc
  * 8.2 App Store, iTune-Connect
* 9. Process Improvement. You can probably guess that my ex-employers talked in CMMI and Six Sigma.

The step are purposely numbered for easy reference and ordering through whole website/repository.
