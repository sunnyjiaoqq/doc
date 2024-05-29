# AutoConfig Bot



The [AutoConfig bot](https://app.myshell.ai/bot/MR3uEz/1712487949) is designed to make it easier to build up a Pro Config based on your idea. It can automatically generate the framework of Pro Config as well as recommend suitable widgets you may need. The Pro Config is generated page-by-page, and all you need to do is provide the description of each page in natural language. You can also correct or modify the config during the generation. Below are the details instructions:

### Basic Usage

* After the bot starts, you can click the `Create Page` button to enter the page name and the description of that page. You need to make sure your description contains detailed usage of the page, including the inputs from the user, what types of tasks to perform, and which variables to display. Please see the default description for an example.
* If you are satisfied with the generated result, you can click the `Confirm` button to move to the next step.
* If you want to modify the outputs at a specific step, you can click the `Update` button and choose the corresponding name of the generator and input your instructions.
* After the generation of each page, you can click the `Create Transition` button to add transitions between the pages or click the `Export` button to get the full Pro Config result.

### Limitations

* Currently, AutoConfig only provides you a draft of Pro Config. You need always check the outputs of each AnyWidgetModule and rename them accordingly (for example, `result.file_urls[0]`)
* This AutoConfig bot is in Beta version. Although we have added many checkers during the generation, we can not assure the generated Pro Config can be executed perfectly. You may need to examine the generated Pro Config and report to our dev team if you encounter any issues.



### Step-by-Step Tutorial

First, go to the [AutoConfig bot](https://app.myshell.ai/chat?bot=1\&shareCode=MR3uEz\&botId=1712487949) and clear the memory to start a new chat. After clicking the `Start` button we will see a welcome message:

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

we can clickthe `Create Page` button and input the page name and the description:

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

the result is then returned as

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Note that the message only shows an intermediate result, not the Pro Config. If we are satisfied with the result, we can click the `Confirm` button to continue

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Here the `inputs_names` and `render_names` are returned, and we need to pay attention to the generator name  `first_page:inputs_render_names` . It would be useful if we want to update the result later. Here we still click the `Confirm` The returned result is:

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

In this step, we obtain the details of inputs and render, which is already in the format of Pro Config. We then click the `Confirm` button:

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

This step generates the whole workflow, consisting of multiple modules and the corresponding purposes and usages. Since these results are good, we click the `Confirm` button:

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

We then obtain the recommended widgets to implement the workflow. We can also click the widget\_url to check if the widget can achieve our goal.&#x20;

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

In this step we get the input and output variable names of each widget. As an example, we assume we want to modify some of the variable names. We click the `Update` button and select thegenerator and input the instruction:

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

The updated result is then displayed as:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

As we can see, the input variable of sentence\_construction has been successfully modified. In the next step, we will generate the `module_config` of each module, which could be time-consuming, please be patient.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

One thing we need to note is that the output\_name might be different from the actual usage of the widgets. We always  need to check the Pro Config template of each widget.

Now we have created a whole page. We can also create a transition by clicking the `Create Transition` button:

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

We simply create a button  `Default Button` that can jump to the first\_page itself. When we are satisfied with the result, we can click the `Export` button to obtain the full Pro Config

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

