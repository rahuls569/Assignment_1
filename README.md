For this Assignment following producer is adopted:
1 Mnist image and random number are taken from the dataset. In the dataset, image, label, random number and addition of random number and label are returned from the get item. The length of the dataset is equal to the length of image.
![image](https://user-images.githubusercontent.com/79099957/211877718-b004b96f-6393-446d-97db-b74920c3427b.png)
![image](https://user-images.githubusercontent.com/79099957/211876559-1a9aa47f-df39-4f99-af7e-ecfebfcfdc45.png)

Now data loader is used to make the batches.
![image](https://user-images.githubusercontent.com/79099957/211876794-f5fd430f-9f80-403e-be69-846f61f17170.png)

A neural network is defined which has two input (Mnist image and a random number). The image layer and random number is added inside it. Two output are taken: one for mnist image (0-9) and second for addition (0 to 18).
Now a fake image and random number is passed into the neural network and check the prediction for the two outputs.
torch.set_grad_enabled(True) is used to allow computation of gradients using backpropagation
for training on the GPU : device = torch.device("GPU").
Adam is used for optimizer.
now 32 size of batches is passed to the network and loss1 and loss2 functions are calculated
