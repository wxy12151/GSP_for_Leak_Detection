# Debug Notes

## 1. version conflict problem:

When the torch_geometric package installed in your environment is a newer version than the author

you will see: 'ChebConv' object has no attribute 'weight' when you run reconstruct.py

Problem: torch_geometric.nn.ChebConv has been updated signficantly, so there are too many differences than before.

Solution: you should go to [ChebConv packet Commits on Oct 12, 2020](https://github.com/pyg-team/pytorch_geometric/blob/f5f200759407806c19f00b46919de3ff6eed4385/torch_geometric/nn/conv/cheb_conv.py), and replace the ChebConv installed in your computer to the code in the above link.