Gynaptic
========
Gynaptic is a modification of [Synaptic](https://github.com/cazala/synaptic), adding methods to insert genetic algorithms in your code. Numerous of mutation, crossover and selection methods are created so you don't have to create your own. 

## Usage
This is simple documentation on how to use the methods. Once the project has been sufficiently attributed, I will add a Wiki going into debt of each method and showing how you can add your own.

###### Mutation methods
There are 4 mutation methods at the moment. More will be added in the future.
```javascript
Mutate.SWAP_WEIGHT // swaps to random connection weights
Mutate.SWAP_BIAS // swaps to random neuron biases
Mutate.MODIFY_RANDOM_WEIGHT // adds or substracts a random value from a random connection weight
Mutate.MODIFY_RANDOM_BIAS // adds or substracts a random value from a random neuron bias
// more to come
```
Each of these mutation methods can be used on the `Neuron`, `Layer` and `Network` objects. At the moment, the methods are only ready for Layers. They other objects will be done soon.

Please notice that mutation will clear contextual data of your neural object at the moment! This will stay until a workaround is discovered. You can use each of the methods like so:
```javascript
var layer = new Layer(4);
layer.mutate(Mutate.SWAP_WEIGHT); // e.g.
```

###### Crossover methods
Work in progress, planned methods:
```javascript
Crossover.SINGLE_POINT
Crossover.TWO_POINT
Crossover.UNIFORM
// more to come
```

###### Selection methods
Work in progress, planned methods:
```javascript
Selection.ELITISM
Selection.FITNESS_PROPORTIONATE
// more to come
```
Some of the selection methods will be combinable with others.
