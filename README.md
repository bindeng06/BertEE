# BertEE
Use BERT for event extraction and Use R_drop for data augmentation
dateset：ACE 2005 corpus
# Prerequisites
1.ACE 2005 dataset in the same format as the [data/sample.json]

2.Install the packages.
```sh
pip install pytorch==1.0 pytorch_pretrained_bert==0.6.1 numpy
```
# Train
```sh
python train.py
```

# Evaluation
```sh
python eval.py --model_path=latest_model.pt
```

# Result
<table>	
  <tr>	
    <th rowspan="2">Method</th>	
    <th colspan="3">Trigger Classification (%)</th>	
    <th colspan="3">Argument Classification (%)</th>	
  </tr>	
  <tr>	
    <td>Precision</td>	
    <td>Recall</td>	
    <td>F1</td>	
    <td>Precision</td>	
    <td>Recall</td>	
    <td>F1</td>	
  </tr>	
  <tr>	
    <td>JRNN</td>	
    <td>66.0</td>	
    <td>73.0</td>	
    <td>69.3</td>	
    <td>54.2</td>	
    <td>56.7</td>	
    <td>55.5</td>	
  </tr>	
  <tr>	
    <td>JMEE</td>	
    <td>76.3</td>	
    <td>71.3</td>	
    <td>73.7</td>	
    <td>66.8</td>	
    <td>54.9</td>	
    <td>60.3</td>	
  </tr>	
  <tr>	
    <td>BERT base</td>	
    <td>63.4</td>	
    <td>71.1</td>	
    <td>67.7</td>	
    <td>48.5</td>	
    <td>34.1</td>	
    <td>40.0</td>	
  </tr>	
	<tr>	
    <td>This model (BERT base + R_Drop)</td>	
    <td>64.8</td>	
    <td>74.6</td>	
    <td>69.4</td>	
    <td>52.1</td>	
    <td>35.0</td>	
    <td>41.9</td>	
  </tr>	
</table>	

## Reference
* lx865712528's EMNLP2018-JMEE repository [[github]](https://github.com/lx865712528/EMNLP2018-JMEE)
* nlpcl-lab/bert-event-extraction [[github]](https://github.com/nlpcl-lab/bert-event-extraction)
* R_Drop[[知乎]](https://zhuanlan.zhihu.com/p/418305402)


