# seq2seq-Transformer
## Enviorment

* Install Pytorch
```
conda install pytorch torchvision cudatoolkit=10.0 -c pytorch
```
* Install pytorch-pretrained-bert
```
pip install spacy ftfy==4.4.3
python -m spacy download en
pip install pytorch-pretrained-bert
```
* Install pyrouge
```
pip install pyrouge
```

## Parameters

### Searching
```
searching method: str (default BFS_BEAM)
    BFS_BEAM: BFS Beam Searching method
    AStar: AStar Beam Searching method

beam_size: int (default 5)
    beam size of the searching

answer_size: int (default 5)
    how many answers you want search at most

gen_max_limit: int
    limit for generated tokens/subwords  

cands_limit: int (default 100,000)
    For AStar searching only, the memory limit for the Splay Tree.

gamma_value: float (default 14.0)
    The \eta value for bi-Gram Trick

similar_smoothing: bool (default False, action set True)
    Whether use similar_smoothing or not
```

### Reranking

```
reranking_method: str (default: smooth_bound_reward)
    length_norm:
    bp_norm:
    bp_unigram_norm:
    bp_bigram_norm:
    bounded_word_reward:
    bounded_adaptive_reward:
    smooth_bound_reward:
```