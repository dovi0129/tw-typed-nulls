# Edge lists

Edge lists of all 11-neuron graphs used in "Does Connectome Wiring Help a Recurrent Controller? A Test Against Typed
Degree-Preserving Nulls" (AAAI-27 Student Abstract).

`graphs.json` contains 23 graphs:

| family | graphs | description |
|---|---|---|
| `tw` | 1 | *C. elegans* tap-withdrawal circuit (topology and polarity only) |
| `typed_null` | 6 | typed degree-preserving nulls of TW: every neuron keeps its in- and out-degree per chemical type and its gap-junction degree |
| `total_preserving_null` | 6 | nulls that keep only the network-wide count of each synapse type |
| `ablation_rewired` | 6 | each total-preserving null after typed double-edge swaps (keeps its typed degrees, changes partners) |
| `ablation_motor_narrowed` | 4 | the first four total-preserving nulls with one excitatory interneuron input per motor neuron, as in TW |

Neurons 0, 1, 6, 7 are sensory, 2, 3, 4, 5, 8 are interneurons, and 9, 10 are motor neurons. Chemical synapses are
directed (`pre` → `post`) and are excitatory or inhibitory. Each gap junction is listed once and acts in both directions.
All graphs have 9 excitatory and 17 inhibitory chemical synapses and 2 gap junctions, receive no chemical input at
sensory neurons, send no output from motor neurons, and reach both motor neurons from the sensory neurons. Each entry
also gives the number of chemical inputs to the motor neurons and of direct sensory-to-motor synapses.

The TW topology is taken from `generate_circuits/tw_pure.bnn` of the neuronal circuit policies repository
(https://github.com/mlech26l/neuronal_circuit_policies); neuron indices follow that file.
