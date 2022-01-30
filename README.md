# Tackling-the-Longtail-for-GNNs
The 'Inductive-' files are for experiments on inductive settings. The 'Transductive-' files are for experiments on transductive settings. 

The commands are as follows:

For 'Inductive-original', the command can be
python main.py --data cora --model GCN --epochs 1000
Parameter 'data' can be Cora, Citeseer, Pubmed with 'data = geo_data.Planetoid(os.path.join(DATA_ROOT, data_name), data_name).data', CS with 'data = geo_data.Coauthor(os.path.join(DATA_ROOT, data_name), data_name).data'. If use other dataset, this parameter is not necessory to be set.
Parameter model can be GCN, SGC, and GAT.

For 'Inductive-RS', 'Inductive-RW', and 'Inductive-BBN', the command can be 
python main.py --data cora --model GCN --epochs 1000 --mode 1
Parameter mode can be 1, 2, and 3 for three weighting strategies, respectively. The other parameters are similar to the 'Inductive-original'.

For 'Inductive-ML', the command can be 
python main.py --data cora --model GCN --epochs 1000 --topk_neg 0.1 --topk_pos 0.1 --topn 0.1 --anchor_sample_ratio 0.5 --margin 0.2

For transductive settings, the mode is only set 1. The other parameters are similar to inductive settings.
