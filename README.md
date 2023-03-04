# EMI-calculator-app-automation-made-by-appium-and-selenium

### Test scenarios
If an user take loan (?) tk from a bank with interest of (?)% and  want to give (?) tk per month as EMI (installment) and processing fee (?)%, how many time period it will take to complete the loan? Take the values from dataset and assert the monthly EMI, total interest, processing fee amount and total payment from the result view. (See below image)

For solve this question, create a dataset using following values: <br>

Amount | Interest | EMI | Processing Fee | Monthly EMI | Total Interest | Processing Fee | Total Payment | Period (Year) | Period (Month) <br>

100000 | 6 | 2000 | 2% | 2000 | 15361.08 | 2000 | 115361.08 | 4 | 10 <br>
200000 | 8 | 5000 | 2% | 5000 | 33391.61 | 4000 | 233391.61 | 3 | 11 <br>
250000 | 7 | 8000 | 1.5% | 8000 | 26804.51 | 3750 | 276804.51 | 2 | 11 <br>
50000 | 10 | 1000 | 5% | 1000 | 14949.12 | 2500 | 64949.12 | 5 | 5 <br>

### How I done this project
- Downloaded google EMI calculator for android
- put it in d drive
- Opened Android studio
- Opened emulator 
- Opened APK file
- Played the emulator
- Put ```adb devices``` this command on cmd to ensure emulator device is working or not
- Put ```appium -p 4723``` this command on cmd to open appium server
- Opened Appium inspector
- Set desired capabilites in json format: <br>
{  <br>
  "appium:deviceName": "emulator",  <br>
  "appium:uuid": "emulator-5554",  <br>
  "platformName": "Android",  <br>
  "appium:platfromVersion": "11",  <br>
  "appium:appPackage": "com.continuum.emi.calculator",  <br>
  "appium:appActivity": "com.finance.emicalci.activity.Splash_screnn",  <br>
  "appium:app": "D:\\APK\\emicalculator.apk"  <br>
  }  <br>
  
  - Ensured the connectivity between emulator and appium inspector
  - Opened Intellij Idea
  - do the expected tests in calculator
  -  Put ```gradle clean test``` this command in the terminal to see the test result
  - Put ```allure generate allure-results --clean -o allure-report``` and ```allure serve allure-results``` commands to generate reports
