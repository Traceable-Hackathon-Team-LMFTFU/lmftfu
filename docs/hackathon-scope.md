# Project Lifecycle

For the Traceable Hackathon 2023, we are defining the following scope in this project -

1. Suggest the best deployment strategy to a customer.
2. Suggest top few best deployment strategies along with a customised list of pros/cons specific to the customer's use-case.
3. Create an interface to take necessary inputs for the above.


## Plan
### Finding the best deployment strategy
There are two approaches to this -
1. Create a set of attributes based on which the `LMFTFU` assistant may figure out the best deployment strategy.
2. For each deployment strategy that Traceable provides, create the following sets and based on these, get a better understanding of how best to train the assistant to find the optimal strategy -
   1. A feature set capturing all the capabilities of the strategy.
   2. A requirement set capturing all the limitations of the strategy.

We will create a decision tree qualifier once we have the set of attributes as mentioned in point 1 above. We would like to feed a wide range of input scenarios to this qualifier so that it is trained as much as possible.

##### Future scope
Whenever a customer uses the interface that is created for this hackathon, we can store the inputs provided by the customer, and once we know what deployment strategy they ended up using, we can update our qualifier with an additional row of input to train it better.

Which strategy was used by the customer will be known quite some time after they actually query our assistant. So we will need to store the inputs provided to the assistant in the beginning of POV, and somehow connect it to the final strategy that was chosen and turned out to be successful.


### Finding the top few best deployment strategies
Here we need our qualifier to score all possible strategies based on the inputs, and provide the top scoring strategies as a result.

We also want to provide a tailored list of pros and cons for each suggested strategies, if any, based on what inputs were gathered.

##### Future scope
1. Assistant is able to answer doubts regarding any of the suggested deployment strategy.
2. Assistant is able to talk about various UI features like API Catalog, Discovery, Risk, Protection, etc as well when talking about the deployment strategies and its pros/cons.


### Creating an Interface
We can interact with the prospect in various ways -
1. Chatbot which prompts you to extract the required information for deciding the best deployment strategy.
2. Google Sheet which takes a predefined set of input and provides you a detailed summary of the best deployment strategy.
