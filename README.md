 ## `Learning rule`
 
Learning rule is a method or a mathematical logic. It helps a Neural Network to learn from the existing conditions and improve its performance. It is an iterative process.

Learning rule or Learning process is a method or a mathematical logic. It improves the Artificial Neural Network’s performance and applies this rule over the network. Thus learning rules updates the weights and bias levels of a network when a network simulates in a specific data environment.
Applying learning rule is an iterative process. It helps a neural network to learn from the existing conditions and improve its performance.
# Hebbian Learning Rule 
Hebbian learning rule – It identifies, how to modify the weights of nodes of a network.
- Also known as 'Hebb Learning Rule', was proposed by 'Donald O Hebb'.
- One of the 'first' and also easiest learning rules in the neural network. 
- It is a single layer neural network, i.e. it has one input layer and one output layer. 
- The input layer can have many units, say n. The output layer only has one unit. 
- Hebbian rule works by updating the weights between neurons in the neural network for each training sample.

## Hebbian Learning Rule Algorithm

- Set all weights to zero, `wi = 0` for `i=1 to n`, and `bias to zero`.
- For each `input vector`, `S(input vector)` : `t(target output pair)`, repeat steps 3-5.
- Set activations for input units with the input vector `Xi = Si` for `i = 1 to n`.
- Set the corresponding output value to the output neuron, i.e. `y = t`.
- Update weight and bias by applying Hebb rule for all `i = 1 to n`:

![image](https://github.com/Siddhipatade/Hebbian-rule/assets/91780318/499a6d53-cea5-4048-84b4-708d81e1a567)

### Implementing AND gate using Hebb Rule

![image](https://github.com/Siddhipatade/Hebbian-rule/assets/91780318/7653fc5a-ae1e-4223-8f68-068f4c1dd527)

- There are 4 training samples, so there will be 4 iterations. Also, the activation function used here is Bipolar Sigmoidal Function so the range is [-1,1]. 
- Step 1 : 
	Set weight and bias to zero, w = [ 0 0 0 ]T  and b = 0.
- Step 2 : 
 Set input vector Xi = Si  for i = 1 to 4.
	X1 = [ -1 -1 1 ]T
	X2 = [ -1 1 1 ]T
	X3 = [ 1 -1 1 ]T
	X4 = [ 1 1 1 ]T
- Step 3 : 
	Output value is set to y = t.

- Step 4 : 
	Modifying weights using Hebbian Rule:
	
 First iteration – 
	w(new) = w(old) + x1y1 = [ 0 0 0 ]T + [ -1 -1 1 ]T . [ -1 ] =   [ 1 1 -1 ]T

For the second iteration, the final weight of the first one will be used and so on.
	
 Second iteration –
	
 w(new) = [ 1 1 -1 ]T + [ -1 1 1 ]T . [ -1 ] = [ 2 0 -2 ]T
	
 Third iteration – 
	
 w(new) = [ 2 0 -2]T + [ 1 -1 1 ]T . [ -1 ] = [ 1 1 -3 ]T
	
 Fourth iteration – 
	
 w(new) = [ 1 1 -3]T + [ 1 1 1 ]T . [ 1 ] = [ 2 2 -2 ]T
	
 So, the final weight matrix is [ 2 2 -2 ]T

![image](https://github.com/Siddhipatade/Hebbian-rule/assets/91780318/20c3fb04-4126-4a38-a609-167ad054a7f8)
