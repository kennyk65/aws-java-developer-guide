.. Copyright 2010-2016 Amazon.com, Inc. or its affiliates. All Rights Reserved.

   This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0
   International License (the "License"). You may not use this file except in compliance with the
   License. A copy of the License is located at http://creativecommons.org/licenses/by-nc-sa/4.0/.

   This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
   either express or implied. See the License for the specific language governing permissions and
   limitations under the License.

#########################
Using the SDK with Gradle
#########################

To use the SDK in your Gradle_ project, use Spring's `dependency management plugin
<https://github.com/spring-gradle-plugins/dependency-management-plugin>`_ for Gradle, which can be
used to import the SDK's Maven Bill of Materials (BOM) to manage SDK dependencies for your project.

**To configure the SDK for Gradle**

1. Add the dependency management plugin to your :file:`build.gradle` file::

    buildscript {
        repositories {
            mavenCentral()
        }
        dependencies {
            classpath "io.spring.gradle:dependency-management-plugin:0.5.4.RELEASE"
        }
    }

    apply plugin: "io.spring.dependency-management"

2. Add the BOM to the *dependencyManagement* section of the file::

    dependencyManagement {
        imports {
            mavenBom 'com.amazonaws:aws-java-sdk-bom:1.10.47'
        }
    }

3. Specify the SDK modules that you'll be using in the *dependencies* section::

    dependencies {
        compile 'com.amazonaws:aws-java-sdk-s3'
        testCompile group: 'junit', name: 'junit', version: '4.11'
    }

Gradle will automatically resolve the correct version of your SDK dependencies using the information
from the BOM.

.. note:: For more detail about specifying SDK dependencies using the BOM, see
   :doc:`java-dg-using-maven`.

