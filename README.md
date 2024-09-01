# Effective Water Temperature Forecasting with Transformer

The repo is the implementation for the paper of "Effective Water Temperature Forecasting with Transformer". The paper includes models that are being used from the paper: [iTransformer: Inverted Transformers Are Effective for Time Series Forecasting](https://arxiv.org/abs/2310.06625).


## Usage 

1. Install Pytorch and necessary dependencies.

```
pip install -r requirements.txt
```

2. The datasets are provided in the *target_data* directory

3. To reproduce the results, the model can be run and evaluated using an example command as such:
```
python -u run.py --is_training 1 --root_path ./target_data --data_path data.csv --model_id test --model iTransformer --data custom --features MS --target WaterTemperature --seq_len 24 --label_len 24 --pred_len 24 --e_layers 3 --enc_in 7 --dec_in 7 --c_out 1 --des '1 Days History' --d_model 512 --d_ff 512 --itr 1 --train_epochs 10 --do_predict --inverse
```

Further information can be found by running the `python run.py --help` command.

## Acknowledgement

We appreciate the following GitHub repos a lot for their valuable code and efforts.
- iTranformer (https://github.com/thuml/iTransformer)
- Reformer (https://github.com/lucidrains/reformer-pytorch)
- Informer (https://github.com/zhouhaoyi/Informer2020)
- FlashAttention (https://github.com/shreyansh26/FlashAttention-PyTorch)
- Autoformer (https://github.com/thuml/Autoformer)
- Stationary (https://github.com/thuml/Nonstationary_Transformers)
- Time-Series-Library (https://github.com/thuml/Time-Series-Library)
