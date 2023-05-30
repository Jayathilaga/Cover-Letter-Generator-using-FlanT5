To fit the model in colab the following parameter were used.

1. per_device_train_batch_size=8
2. gradient_accumulation_steps=8

To reduce the training loss and validation loss steps were increased.

1. max_steps=100


Output for 100 steps:

```
1. Step	Training Loss	Validation Loss	     Rouge1	   Rouge2	   Rougel	  Rougelsum	Gen Len
2. 50	  2.065400	        1.617432	     4.993300	  4.175800	4.932800	4.975000	19.000000
3. 100	1.910300	        1.591844	     4.906300  	4.072000	4.888400	4.897300	19.000000
```

generation_config parameters:

1. temperature=2.0

 The value used to module the next token probabilities. So that the generation does not repeat itself.

2. num_return_sequences=3

We are checking for top 3 return sequences to see which one is more preferable. It is mostly the first one.


**Generated Output:**

```
Amy Chan 
(212) 667-5656 
amy.chan@email.com 
February 1, 2018 

Dear Hiring Manager, 
I want to apply for the job of Medical Records Clerk at a hospital in Charlotte.
```
