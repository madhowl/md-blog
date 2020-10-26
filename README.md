#Техническое задание

## Разработать приложение для решения следующей задачи.

Дан каталог ***content*** имеющий следующую структуру:

![](doc/1.png)

0. создать класс ___App___ который должен иметь следующие методы:
    0. getFileList($dir) *-> возвращает массив файлов в указанном каталоге $dir*
    0. getFileContent($file) *-> возвращает содержимое указанного файла $file*
    0. getUri()*-> возвращает URI*
    0. parseUri($uri) *-> возвращает массив из элементов URI*
    0. getDirList($dir)*-> возвращает массив директорий в указанном каталоге $dir* 
    0. main()*-> главный метод выполняющий всю логику приложения*
    
0. Приложение должно реализавать следующую логику 
    1. должно отслеживать содержание URL и парсить содержимое URI в массив
    2. если URI[0] пустой возвращать значение файла index.md  
    4. иначе проверить сущиствование файла совподающего со значением в URI[0]
        1. если файл существует вывести его содержимое на сайт
        2. иначе вернуть ошибку ***404***
    3. если URI[0] = 'blog'  получить список файлов из каталога ___blog___ и вывести краткое содержание записей со ссылкой на прочтение полного материала (ссылка должна иметь вид -> /blog/20-10-2020-som-news.html)
    4. если URI имеет следующий вид /blog/ ___имя файла___ .html проверить существование файла и вывести его содержимое на сайт
    
0. файл страница должен соответствовать следующим требованиям :
    1. основное контент хранится в формате ***MarkDown***
    2. в файле должна присутствовать секция в формате **JSON** содержащая - Заголовок, дату публикации, вводный текст поста и ссылку на изображение к вводному тексту.
    
