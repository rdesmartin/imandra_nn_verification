## Imandra Neural Network Verification Library

### Dissertation 

The full dissertation is at `/H00359321_masters_thesis.pdf` 

### File hierarchy

This repository holds the code for the Master's dissertation *Neural Network Verification With Imandra*.
The code is separated into 4 parts:

* `preliminary`: the naive implementation of feed-forward NN in IML (Section 4.1)

* `cnn_library`:
  - the library for representing convolutional neural networks (CNN) in IML (Section 4.2). Main file: `top.iml`
  - code for experiments on filter properties (Section 5.2). Main file: `filter_properties.iml`

* `cnn_library_quantised`: 
  - the quantised version of the previous library, necessary to use Imandra's Blast strategy (Section 4.2.7). Main file: `top.iml`
  - the implementation of multiple definitions of robustness (Section 4.3), and the evaluation of these multiple definitions (Section 5.1). Main file: `top.iml`
  - the evaluation against an ACAS Xu benchmark model (Section 5.3). Main file: `acas_xu.iml`

* `notebooks`: 
  - the python notebooks used to train the network and containing the script to convert trained networks to IML
  - the serialised networks in Keras' serialisation format

### Execution of IML code

The execution of IML code is done via the Imandra CLI. To execute one of the experiments, launch Imandra CLI from the main file's directory and enter the following commands:

```
$ #redef;;
$ #use "top_file_name.iml";;
```

The functions defined in the main file can then be used in the interactions with the CLI.
