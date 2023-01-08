# Задание 6

Задача: с некоторых новостных сайтов были загружены тексты новостей за период  несколько лет, причем каждая новость принаделжит к какой-то рубрике (*science*, *style*, *culture*, *life*, *economics*, *business*, *travel*, *forces*, *media*, *sport*). Нужно написать программу, которая автоматически определяет к какой рубрике можно отнести новость. Данные расположены в архиве, который можно загрузить  [здесь](https://raw.githubusercontent.com/alexmk7/pm_task_2016/master/news_data.zip), тестовый сервер здесь: http://52.200.49.43/2016it/news . В файле **news_train.txt** 60,000 строк, в каждой строке содержится метка рубрики, заголовок новостной статьи и сам текст статьи, например:

>    **sport**&nbsp;&lt;tab&gt;&nbsp;**Сборная Канады по хоккею разгромила чехов**&nbsp;&lt;tab&gt;&nbsp;**Сборная Канады по хоккею крупно об...**

где &lt;tab&gt; символ табуляции. В файле **news_test.txt** 15,000 строк, на каждой строке заголовок и новость без метки. Задача -- предсказать категорию всех новостей из тестового файла. 


# Решение

В качестве вспомогательной библиотеки был выбран пакет scikit-learn. (news.py)
  1. Чтение и обработка текстов с целью получения набора векторов-признаков.
  2. Преобразование количества слов в частоты. (tf–idf)
  3. Обучение классификатора (SVM)
  4. Получение результатов
