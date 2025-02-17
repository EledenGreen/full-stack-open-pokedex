Our application is a simple 2-D Windows game developed using C++.

For our CI/CD pipeline, we follow the following steps:

1.  Linting: It is the process of analyzing our codebase for any programming errors, stylistic errors, etc. Currently we are using [cpplint](https://github.com/cpplint/cpplint) and it has helped our team maintain a consistent and quality codebase.
2.  Testing: Testing is critical in our pipeline to check whether our application is behaving as it is supposed to be. We practice unit test, End-to-End test before and after build. Currently we are using [googletest](https://github.com/google/googletest) and it supports any kind of test.
3.  Building: Our source code is compiled using [CMake](https://cmake.org/) which is free and cross-platform.

Now, using Bitbucket, the source code is versioned controlled and linting is configured. Then, Cmake is configured for automatic build for every commit on the main branch. It is than tested using googletest.

Currently we are opting for Bitbucket Cloud-based CI/CD because:

1.  We are a small team of 5 members.
2.  No need to invest in physical infractructure.
3.  Easy to start configuring pipelines.
4.  More cost effective for our small application.
5.  Can scale as per requirements.
6.  Ease of integration of other development tools.
