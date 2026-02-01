## trading_record_prompt.md
## Objective:
Reading config file --read-cfg <filename> default is trading_reocrd_cfg.yaml
Reading data_history --read-history <filename> default is trading_record_history.yaml
read history protocol may change base on its file extension, could be .yaml, .pickle, .zip
create session config object base on cfg
Reading data file designated by --data <filename>
Parsing data add into pf
append data to df
at the end output data --output-history <filename> default is same as read history 
