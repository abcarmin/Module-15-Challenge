# Module-15-Challenge

For this project, I am utilizing Python, Jupyter Lab, and Amazon Web Services to create a robo advisor that provides investment portfolio recommendations for retirement. I will create, build, and test the initial robo advisor using Amazon Lex bot. Then, I will enhance the robo advisor using an Amazon Lambda function to provide the recommendation.

---

## Technologies

This project uses pandas programming language and utilizes Anaconda, Python, Git Bash, Jupyter Lab, Github, and Amazon Web Services. This project also uses an Amazon Lambda function and Amazon Lex bot within AWS.

---

## Installation Guide

These are the required libraries and dependencies:

from datetime import datetime

from dateutil.relativedelta import relativedelta


---

## Usage

* I configured the initial robo advisor and provided utterances:

Bot name: RoboAdvisor

Language: English (US)

Output voice: Salli

Session timeout: 5 minutes

Sentiment analysis: No

COPPA: No

Advanced options: No

All other options: The default value


Sample Utterances:

I'm {age} and I want to invest for my retirement

I want the best option to invest for my retirement

I'm worried about my retirement

I want to invest for my retirement


* I built and tested the robo advisor:

    
Screenshots from the provided Amazon Lex Bot Video:
    
![Screenshot 1](https://github.com/abcarmin/Module-15-Challenge/blob/main/Amazon%20Lex%20bot%20Screenshot1.png)

![Screenshot 2](https://github.com/abcarmin/Module-15-Challenge/blob/main/Amazon%20Lex%20bot%20Screenshot2.png)

![Screenshot 3](https://github.com/abcarmin/Module-15-Challenge/blob/main/Amazon%20Lex%20bot%20Screenshot3.png)
    

* I enhanced the robo advisor with an Amazon Lambda Function:

Additional code that was added to provide validation rules and recommendations:

    if age <= 0: 
            return build_validation_result(False, "age", "You must be older than 0 years old.")
        elif age >= 65:
            return build_validation_result(False, "age", "Your must be younger than 65 years old.")
            
    if investment_amount < 5000:
            return build_validation_result(False, "investmentAmount", "The investment amount must be greater than or equal to $5,000.")
    
    def get_recommendation(risk_level):
        risk_level = risk_level.lower()
        if risk_level == "none":
            return "100% bonds (AGG), 0% equities (SPY)"
        elif risk_level == "low":
            return "60% bonds (AGG), 40% equities (SPY)"
        elif risk_level == "medium":
            return "40% bonds (AGG), 60% equities (SPY)"
        elif risk_level == "high":
            return "20% bonds (AGG), 80% equities (SPY)"

Screenshots from the provided Amazon Lex with Lambda Video:
    
![Screenshot 1](https://github.com/abcarmin/Module-15-Challenge/blob/main/Lex%20with%20Lambda%20Screenshot1.png)

![Screenshot 2](https://github.com/abcarmin/Module-15-Challenge/blob/main/Lex%20with%20Lambda%20Screenshot2.png)

![Screenshot 3](https://github.com/abcarmin/Module-15-Challenge/blob/main/Lex%20with%20Lambda%20Screenshot3.png)

![Screenshot 4](https://github.com/abcarmin/Module-15-Challenge/blob/main/Lex%20with%20Lambda%20Screenshot4.png)



---

## Contributors

Allyssa Carmin

---

## License

SMU Fintech Course