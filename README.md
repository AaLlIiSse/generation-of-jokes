# Нейронная сеть, генерирующая анекдоты

В рамках лабораторной работы нужно было дообучить модель, основанную на [русскоязычной GPT-3](https://github.com/ai-forever/ru-gpts)<sup>1</sup>, которая может генерировать связанный текст на основе заданного отрывка. 

Датасет был составлен самостоятельно, на основе сборников анекдотов и [датасета из гита](https://github.com/computational-humor/humor-recognition/tree/master/data)<sup>1</sup>.

В итоге были дообучены две нейросети. 
Вот [jupiter notebook](Вставить сюда загруженный файл юпитрера нейронки по статье) первая модель, которая может сгенерировать что-то вроде

Обучалась по [статье](https://habr.com/ru/amp/post/599673/)<sup>1</sup> из Хабра на основе созданного датасета.

Результат:

> Негр и гей возят на джипах яблоки.

> О современном слэнге. Когда чиновник попавшийся на взятке кричит Меня подставили!!! перевод А почему всем можно, а мне нет.
 
Выглядит неплохо..?

Вторая нейронка дообучена на той же модели от сбербанка.
Вот [её jupiter notebook](https://github.com/TIoJIuHa/generation-of-jokes/blob/main/joke_training_model.ipynb)<sup>1</sup>.

Она генерирует результаты похуже

> Это означает, что можно будет купить новую квартиру и не бояться.  А вы?  Может быть, и правы.  А все ли ваши друзья так боятся?  Нет, конечно.  Это все предрассудки.  Например, некоторые считают, что если человек ходит в джинсах и майке, то ему все равно.  Но на самом деле, он не одевается, он ходит в джинсах.

## Проблемы с обучением

Основная проблема была в том, что "sberbank-ai/rugpt3large_based_on_gpt2" слишком тяжёлая для ноутбуков. Устройства отрубались, выдавая ошибку *памяти cuda*. Проблема решилась после смены трансформера на "sberbank-ai/rugpt3lsmall_based_on_gpt2" - small. Однако и качество генерируемого текста сильно упало. 

## Литература 

https://habr.com/ru/amp/post/599673/

https://huggingface.co/




