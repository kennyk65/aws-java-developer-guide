.. Copyright 2010-2016 Amazon.com, Inc. or its affiliates. All Rights Reserved.

   This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0
   International License (the "License"). You may not use this file except in compliance with the
   License. A copy of the License is located at http://creativecommons.org/licenses/by-nc-sa/4.0/.

   This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
   either express or implied. See the License for the specific language governing permissions and
   limitations under the License.

################
SDK Code Samples
################

The |sdk-java| comes packaged with a number of code samples that demonstrate many of the features of
the SDK in buildable, runnable programs that you can study or modify to implement your own AWS
solutions using the |sdk-java|.

.. contents::
   :depth: 1
   :local:

How to get the samples
======================

The |sdk-java| code samples are provided in the `samples` directory of the SDK. If you downloaded
and installed the SDK using the information in :doc:`java-dg-install-sdk`, then you already have the
samples on your system.

You can also view the latest samples on the |sdk-java|'s GitHub repository, in the `src/samples
<https://github.com/aws/aws-sdk-java/tree/master/src/samples>`_ directory.


.. _samples-cmdline:

Building and running the samples using the command line
=======================================================

The samples include `Ant <http://ant.apache.org/>`_ build scripts so that you can easily build and
run them from the command line. Each sample also contains a README file in HTML format that contains
information specific to each sample.

.. tip:: If you are browsing the sample code on GitHub, click the :guilabel:`Raw` button in the source
    code display when viewing the README.html file for a sample. In raw mode, the HTML will render
    as intended in your browser.

Prerequisites
-------------

Before running any of the |sdk-java| samples, you will need to set your AWS credentials in the
environment or with the AWS CLI as specified in :doc:`set-up-creds`. The samples use the default
credential provider chain whenever possible, so by setting your credentials this way, you can avoid
the risky practice of inserting your AWS credentials in files within the source code directory
(where they may inadvertently be checked in and shared publicly).

Running the samples
-------------------

**To run a sample from the command line**

1.  Change to the directory containing the sample's code. For example, if you are in the root
    directory of the AWS SDK download and want to run the :file:`AwsConsoleApp` sample, you would
    type:

    .. code-block:: none

        cd samples/AwsConsoleApp

2.  Build and run the sample with Ant. The default build target performs both actions, so you can
    just enter:

    .. code-block:: none

        ant

    The sample prints information to standard output |mdash| for example:

    .. code-block:: none

        ===========================================

          Welcome to the AWS Java SDK!

        ===========================================
        You have access to 4 Availability Zones.

        You have 0 Amazon EC2 instance(s) running.

        You have 13 Amazon SimpleDB domain(s) containing a total of 62 items.

        You have 23 Amazon S3 bucket(s), containing 44 objects with a total size of 154767691 bytes.


Building and Running the Samples using the Eclipse IDE
======================================================

If you use the |tke|, you can also start a new project in Eclipse based on the |sdk-java| or add the
SDK to an existing Java project.

Prerequisites
-------------

After installing the |tke|, we recommend configuring the Toolkit with your security credentials.
You can do this anytime by selecting :guilabel:`Preferences` from the :guilabel:`Window` menu in
Eclipse, and then selecting the :guilabel:`AWS Toolkit` section.

Running the samples
-------------------

**To run a sample using the AWS Toolkit for Eclipse**

1.  Open Eclipse.

2.  Create a new AWS Java project. In Eclipse, on the :guilabel:`File` menu, point to
    :guilabel:`New`, and then click :guilabel:`Project`. The :guilabel:`New Project` wizard opens.

3.  Expand the :guilabel:`AWS` category, then select :guilabel:`AWS Java Project`.

4.  Click :guilabel:`Next`. The project settings page is displayed.

5.  Enter a name in the :guilabel:`Project Name` box. The AWS SDK for Java Samples group displays
    the samples available in the SDK, as described previously.

6.  Select the samples you want to include in your project by selecting each check box.

7.  Enter your AWS credentials. If you've already configured the |tke| with your credentials, this
    is automatically filled in.

8.  Click :guilabel:`Finish`. The project is created and added to the :guilabel:`Project Explorer`.

**To run the project**

1.  Select the sample :file:`.java` file you want to run. For example, for the |S3| sample, select
    :file:`S3Sample.java`.

2.  Select :guilabel:`Run` from the :guilabel:`Run` menu.

**To add the SDK to an existing project**

1.  Right-click the project in :guilabel:`Project Explorer`, point to :guilabel:`Build Path`, and
    then click :guilabel:`Add Libraries`.

2.  Select :guilabel:`AWS Java SDK`, and then click :guilabel:`Next` and follow the remaining
    on-screen instructions.


