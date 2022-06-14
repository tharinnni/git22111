# Automation Framework Cucumber TestNG and Selenium Java building by Anh Tester

**SOME FEATURES IN FRAMEWORK**

1. Run the parallel test case
2. Read Object web element from Properties file
3. Extent Report
4. Allure Report
5. Send Mail after the run test (Report information and HTML file attachment)
6. Write Log to file
7. Record video and Screenshot test case for failed
8. Read data test from Excel file (xlsx, csv, json,...) with class define fields (param: Client client)
9. Base function in the package: utils, helpers
10. Read data test from Json file
11. Main keyword is WebUI
12. Sample test feature

## **SYSTEM REQUIREMENTS**

- **JDK All version**
- Chrome Browser, Edge Browser
- Setup **Allure**:
  https://mvnrepository.com/artifact/io.qameta.allure/allure-java-commons
  or
  https://anhtester.com/blog/selenium-java/selenium-java-tai-nguyen-cai-dat-moi-truong)
  Download jar and setting Variable Environment as Java JDK

  ![image](https://user-images.githubusercontent.com/87883620/161661705-b8706957-5a26-4faf-8ddf-2f9aef78418e.png)

- **IntelliJ** is the best choice (to change JDK version)

![image](https://user-images.githubusercontent.com/87883620/161707184-7ad558f2-0d7d-4851-bfd6-2796d4e46593.png)

## **HOW TO USE**

**1. Run parallel the test case**

- Run test case in suite XML (**src/test/resources/suites/**)
- Run test case from Maven pom.xml file
  (**mvn clean test**)

  ![image](https://user-images.githubusercontent.com/87883620/161658761-5040e527-b410-46b3-8697-3298523e201d.png)

**2. Read Object web element from Properties file**

![image](https://user-images.githubusercontent.com/87883620/161658681-58f3a183-cbfd-433d-853a-927e4373f51c.png)

**3. Extent Report**

- Insert Framework Annotation as sample:

![image](https://user-images.githubusercontent.com/87883620/161657646-3dd652c6-a310-4006-a0cb-de63e2e87e36.png)

- Value from Enums (src/main/java/anhtester/com/enums)
- Setup on TestListener and BaseTest

![image](https://user-images.githubusercontent.com/87883620/161657754-c29b1ee9-f2fb-44b3-bee0-9f425a7cab6f.png)

**4. Allure Report**

- Open Terminal: **_allure serve target/allure-results_**

![image](https://user-images.githubusercontent.com/87883620/161662507-9e4dc698-e452-4b43-a4f5-9808c81419a2.png)

- Insert **@Step("title/message")** above **_@Test_** or any **_Method_** in the project
- (As sample picture above step 3)

![image](https://user-images.githubusercontent.com/87883620/161657680-af29973d-4e52-451f-b1d6-40b12d182845.png)

![image](https://user-images.githubusercontent.com/87883620/161657689-10365747-ed8f-4ca8-9d84-8060514f216b.png)

**5. Send Mail after the run test**

- Config **true/false** in config.properties
  (**_src/test/resources/config/config.properties_**)
- send_email_to_users=**true** is enable send mail
- Config mail with email and password in **_src/main/java/anhtester/com/mail/EmailConfig.java_**
  Note: enabled Allow less secure apps

![image](https://user-images.githubusercontent.com/87883620/161658851-2aa41091-ac99-45d9-a79f-aaa828052efb.png)

![image](https://user-images.githubusercontent.com/87883620/161659238-88337f69-b742-4cd7-87f2-76670519c8dd.png)

![image](https://user-images.githubusercontent.com/87883620/161710836-8f3eee7c-19ba-410d-8498-5f314e6289a5.png)

**6. Write Log to file**

- Call class: Log.info , Log.pass, Log.error,... (**Log** is a custom global class from Log4j2)
  (**_import anhtester.com.utils.Log.java_**)

![image](https://user-images.githubusercontent.com/87883620/161657858-d333ac1d-9e7b-4c1b-baac-151a237a1fa0.png)

**7. Record video and Screenshot**

- Setup in **_config.properties_** file
  (**_src/test/resources/config/config.properties_**)
- screenshot_passed_steps=yes or no
- screenshot_failed_steps=yes or no
- screenshot_skipped_steps=yes or no
- screenshot_all_steps=yes or no

  ![image](https://user-images.githubusercontent.com/87883620/161657881-5235139a-9982-43c0-ac37-09f22fff1206.png)

**8. Read data test from Excel file**

- Create function with annotaion **DataSupplier** on **_src/main/java/anhtester/com/utils/DataProviderUtils.java_**
- Call the name of **DataSupplier** above in the test cases as DataProvider of TestNG
- Read excel with Map and Hashtable

**9. Base function in the package**

- **_src/main/java/anhtester/com/utils_**
- **_src/main/java/anhtester/com/helpers_**

**10. Read data test from JSON file**

- **JsonUtils** class select the json file path and call **"get"** method with **key**

**11. Main keyword is WebUI**

- WebUI class is main keyword in Framework. It contains common functions
- How to use: WebUI.function_name
- Example: WebUI.setWindowSize(1024, 768), WebUI.screenshotElement(By by, String elementName),...

**12. Call test case sample**

- Run test case TestNG: src/test/java/anhtester/com/projects/website/crm/testcases
- Run test case Gherkin: src/test/resources/suites/RunSuiteFeature.xml
- Or run with maven in **pom.xml** file:  ***mvn clean test***

```
+ src/test/resources/suites/RunSuiteFeature.xml
+ ClientTest
+ SignInTest
+ TestHandle
+ TestSimpleCode
```

## Project structure

```

```

## I shall write document for my Framework. Coming soon...

# Copyright 2022 Anh Tester

> Anh Tester Blog: https://anhtester.com/

![Alt text](https://anhtester.com/uploads/logo/anhtester_logo_512.png?raw=true "Anh Tester - Automation Testing")
