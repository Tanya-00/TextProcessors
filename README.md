# Text Processors
Создаем первый файл text1.txt, командой **touch text1.txt**
![2021-06-04 (1)](https://user-images.githubusercontent.com/62139377/120743629-b88ead80-c53c-11eb-8de0-9e5fcbb06ca2.png)
Затем создаем второй файл, командой **touch text2.txt**. Применяем команду **tail -n 40 text1.txt | cat > text2.txt**, файл выглядит так
![2021-06-04](https://user-images.githubusercontent.com/62139377/120743758-f55aa480-c53c-11eb-9ac7-7853308bb327.png)
Затем создаем третий файл, командой **touch text3.txt**, пишем **head -n 10 text2.txt | cat > text3.txt** вот он ниже
![2021-06-04 (3)](https://user-images.githubusercontent.com/62139377/120743833-16bb9080-c53d-11eb-9c71-751947d9f68b.png)
Дополняем третий файл командой **sed -r 's/koko/kuku/g' text2.txt | grep 'kuku' | head -n 3 | cat >> text3.txt**
![2021-06-04 (4)](https://user-images.githubusercontent.com/62139377/120743907-3a7ed680-c53d-11eb-9a0e-01fd71d6dc62.png)
И финальный штрих **sort text3.txt | uniq -c**
![image](https://user-images.githubusercontent.com/62139377/120743934-45396b80-c53d-11eb-821a-f7e617901867.png)
