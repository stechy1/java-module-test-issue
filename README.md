# java-module-test-issue
Minimal reproduction repository of an issue with including test files from one module to another.

There are two modules in the repository: **submodule1** and **submodule2**. **Submodule2** depends on **submodule1**.
Dependent classes from **submodule1** are visible in **submodule2** without any issues. Same is for _tests_.
So it means it is possible to create an instance of the class **Example1** in the class **Example2**. Same is possible
to do in **Test2** with class **Test1** from **submodule1**.

Now the issue come, when _java modules_ are activated. To do so, rename _module-info.java.txt_ to _module-info.java_.
The compilation fail, because class **Test1** become not visible in class **Test2**.
