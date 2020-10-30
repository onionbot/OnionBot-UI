![Header](https://user-images.githubusercontent.com/32883278/97621285-a4208a80-1a1a-11eb-8b7f-90141d867982.png)

# OnionBot | Python API

<p float="left">
    <img src="https://www.raspberrypi.org/wp-content/uploads/2011/10/Raspi-PGB001.png" height="100"/>
    <img src="https://www.nasuni.com/wp-content/uploads/2019/10/googleCloudPartner.png" height="100"/>
    <img src="https://miro.medium.com/max/400/0*xNxZokzztcgpPueM.png" height="100"/>
    <img src="https://user-images.githubusercontent.com/32883278/84203339-32fb2d80-aaa1-11ea-843e-f7f69da66e53.png" height="50"/>
</p>

*A collaborative computational cooking robot built using computer vision with Raspberry Pi*

Web application for control panel and sous chef interfaces

[See it in action on YouTube](https://youtu.be/W4utRCyo5C4) | 
[Read more about the project on DesignSpark](https://www.rs-online.com/designspark/student-innovation-onionbot-building-a-robot-sous-chef)


### About 

![screens](https://user-images.githubusercontent.com/32883278/97645265-5882d680-1a44-11eb-923b-4e0b824d027c.png)

*Collaborative computational cooking using computer vision. The system combines human and robot cooking: (b) auto management of heating; (c) intelligent reminders and warnings; (d) screen instructions for the human to execute.*

Food image classification is tricky, as food images often have numerous difficult-to-define features and a lot of environmental variation. A new cooking device must tackle these perception problems.

OnionBot introduces two improvements:

- The fixed stove-top camera view ensures a consistent environment
- With general classification, the model must identify characteristics from 1000s of potential classes. Instead, we classify only key events at which actions occur (milestones) for a single recipe. Each model must identify 10s of classes (or less!), dramatically simplifying the perception challenge.

These datasets don’t currently exist, so the `OnionBot-UI` control panel enables easy creation of labelled datasets of cooking images. Simply click along with each milestone as you cook, and labelled images are automatically uploaded to Google Cloud, where they can be accessed by model training platforms. Training is simplified using [Google AutoML](https://cloud.google.com/automl); AutoML allows models to be trained for new recipes with just a few clicks, no ML expertise required!

![goodfood-dc](https://user-images.githubusercontent.com/32883278/97644789-291f9a00-1a43-11eb-965b-ce205b0cad7d.jpg)

*A) Examples from image classes created for the BBC GoodFood tomato sauce recipe. B) The Live Labelling interface makes creating labelled datasets as simple as clicking along with recipe milestones.*

### Known issues 

- Creates inbalanced datasets when some steps take longer than others. Should take a balanced sample from each recipe milestone. 
- AutoML makes training easy, but can get expensive and gives no insight into the model trained


### TODO 

- Improve intuitiveness of recipe following when creating datasets 
- Reduce data cleaning required, move towards automatic model training 

### To connect:

![labelling](https://user-images.githubusercontent.com/32883278/85966412-9cdb6880-b9b7-11ea-9306-bfe3712407bd.png)

1. Start your local web server of choice (we use Apache)
2. Point the server to `onionbot/portal`
3. Start cooking! 


### Interested in building a cooking automation robot?

Get in touch! 




