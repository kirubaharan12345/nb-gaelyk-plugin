Groovy files: Running, Compiling and Testing

# Introduction #

It is posible now to run, compile, test and debug individual .groovy files. All those actions may be executed through a pop-up menu on a .groovy file.

Additionaly,release 0.8.22 adds **Debug Single (Ctrl+Shift+F5)** command. All those commands are available for **Gaelyk** applications autamatically. But now they may be used for both - Web and J2SE applications.


# Run File ( Shift+F6) Menu Item #

When a .groovy file belongs to a **Source packages** of a web or j2se application then it can be executed if it is a _Groovy Script_ or a _Groovy class_ with a main method.

When a Groovy file is a _xxxTest.groovy_  and belongs to a **Test packages** source group of a web  or j2se application then **Run File** action is the same as the **Test File** action.

# Compile File (F9) Menu Item #

Compiles a single .groovy file. May be applied to a Groovy file in a **Source packages** or **Test packages** source group.

# Test File (Ctrl+F6) Menu Item #

If Groovy file is located in a **Test packages** source group then JUnit 4 test case runs. The file must have a suffix "Test".

If the action applies to a Groovy file in a **Source packages** of an application then first finds corresponding .groovy file that has "Test" suffix and executes JUnit 4 test case on it.


# Debug Test File (Ctrl+Shift+F6) Menu Item #

The action applies to a file in a **Source Package** or in a **Test packages** source group. If the action applies to a Groovy file in a **Source packages** of an application then first finds corresponding .groovy file that has "Test" suffix and executes JUnit 4 test case on it.

If Groovy file has a suffix "Test" is located in a **Test packages** source group then JUnit 4 test case runs in debug mode.

If the action applies to a Groovy file in a **Source packages** of the application then first finds corresponding .groovy file that has "Test" suffix and executes JUnit 4 test case on it in debug mode.

# Debug File (Ctrl+Shift+F5) Menu Item #

The action applies to a file in a **Source Package** or in a **Test packages** source group. If the action applies to a Groovy file in a **Test packages** of an application and corresponding .groovy file  has "Test" suffix and then executes JUnit 4 test case on it in debug mode.


# Examples #

> ## Run/Compile Groovy Script ##

  * Create Java package **org.demo**.
  * Create Groovy script. Select the package\*org.demo**and then in an IDE:**File->New->Groovy->Groovy Script**.**

The source might looks like:

```
package org.demo

def name='Guillaume Laforge'

println "Hello $name!"

```

> ## Run/Compile Groovy Class ##

Let's create a Groovy Class (_not script_)

```
package org.demo

class GroovyClass1 {

    def static void main(String[] args) {
        println("This is a GroovyClass1")
    }

    def long add(int i1, int i2) {
        i1 + i2
    }
}

```

You can compile it or run through a popup menu commands such as **Run File** or **Compile File**.

> ## Run/Compile/Test/Debug Groovy Test case ##

First, create JUnit tests using **Tools->Create JUnit Tests**. In a e dialog window select JUnit 4.

Then let's create a Groovy Class that represents a Groovy Test Case. We must do it manually since NetBeans JUnit plugin doesn't support test generation for Groovy classes.

Select **Test packages** and create a class with a name "CroovyClass1Test".

```
package org.demo
import org.junit.Test;
import static org.junit.Assert.*;

/**
 *
 * @author Valery
 */
class DemoClass1Test {
    @Test
    public void testAdd() {
        System.out.println("testAdd");
        int i1  = 4;
        int i2  = 3;
        DemoClass1 instance = new DemoClass1();
        int expResult = 7;
        int result = instance.add(i1,i2);
        assertEquals(expResult, result);
    }
}
```

You can run, compile, test and debug the class using commands such as **Run File** ,**Compile File**,**Test File**, **Debug Test File** or **Debug File**.

If you execute **Run File** on the class _DemoClass1Test_ in a **Test packages** source group it has the same effect as the command **Test File**.

You can execute "Test File/Debug File" on the class _DemoClass1_ in the **Source packages** source group or on the class _DemoClass1Test_. The result will be the same.