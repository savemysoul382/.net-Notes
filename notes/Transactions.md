## Уровни изоляции транзакций

[Шпаргалка .Net](https://habr.com/ru/post/541194/)

- **Read uncommited** (грязное чтение) - самая менее затратная транзакция  
  Если одновременно запустить две транзакции. Внести изменения (insert, update, delete) в первой транзакции, вторая увидит изменения даже до того как первая транзакция их закоммитит.

- **Read commited**  
  Вторая транзакция видит insert, update, delete сделанные в первой транзакции только после коммита первой транзакции.

- **Repeatable read**  
  Вторая транзакция видит insert-ы закоммиченные первой транзакцией, но не видит updat-ы и delet-ы

- S**erializable** - самая затратная, наименьший уровень параллелизма  
  Нельзя работать с данными прочитанными в другой транзакции,
