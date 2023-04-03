# ControlHW
Для решения данной задачи сначала нужно объявить два массива: изначальный и второй (такой же длины). Потом метод, в котором цикл соразмерный длине массива, внутри цикла проверка условия ( <=3 ), если условие верно, элемент первого массива заносится в count элемент второго массива. Переменная count чтобы поочередно закидывать из первого массива во второй и чтобы потом не было пробелов. После присвоения увеличивается переменная count на 1 и возвращается к циклу for в котором i увеличивается на 1. И так проверяется до конца.
![Контрольное дз ГБ](https://user-images.githubusercontent.com/124172672/229623552-f30b7cfd-d351-476e-86a4-ae978daa939f.png)

string[] array1 = new string[5] {"1234", "1567", "hello", "world", "-2"};
string[] array2 = new string[array1.Length];
void SecondArrayWithIF(string[] array1, string[] array2)
{
    int count = 0;
    for (int i = 0; i < array1.Length; i++)
    {
    if(array1[i].Length <= 3)
        {
        array2[count] = array1[i];
        count++;
        }
    }
}

void PrintArray(string[] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"{array[i]} ");
    }
    Console.WriteLine();
}
SecondArrayWithIF(array1, array2);
PrintArray(array2);
