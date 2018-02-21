##Natural Language Understanding with RASA

### Install

> Debian
```{shell, engine='bash', count_lines}
sudo apt-get update
sudo apt-get install python-dev -y
sudo apt-get install python-pip -y
```

> Centos
```{shell, engine='bash', count_lines}
sudo yum install python-devel
```

> RASA

```{shell, engine='bash', count_lines}
sudo pip install rasa_nlu
sudo pip install -U scikit-learn scipy sklearn-crfsuite
sudo pip install sklearn_crfsuite
sudo pip install spacy
sudo pip install sklearn

#IF ERROR
pip install --upgrade --force-reinstall sklearn
```

## Download Language Models

```{shell, engine='bash', count_lines}
python -m spacy download en
python -m spacy download pt
```

### Training
```{shell, engine='bash', count_lines}
python -m rasa_nlu.train -c config/config_spacy.json
python -m rasa_nlu.server -c config/config_spacy.json
```

>> https://github.com/RasaHQ/rasa-nlu-trainer
>> https://rasahq.github.io/rasa-nlu-trainer