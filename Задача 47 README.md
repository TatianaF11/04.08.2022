//Задача 47. Задайте двумерный массив размером m×n, заполненный случайными вещественными числами, 
//округлёнными до одного знака.
// m = 3, n = 4.
// 0,5 7 -2 -0,2
// 1 -3,3 8 -9,9
// 8 7,8 -7,1 9
//void Zadacha47()
{
    Console.WriteLine("Введите количество строк");
    int m = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine("Введите количество столбцов");
    int n = Convert.ToInt32(Console.ReadLine());
         
    double[,] DoubleArray = new  double[m,n];
    CreateDoubleArray(DoubleArray, 10);
    PrintDoubleArray(DoubleArray); 
}

double[,] CreateDoubleArray(double[,] array, int finishNumber)
{
    Random rand = new Random();
    int m =  array.GetLength(0);
    int n =  array.GetLength(1);
    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            array[i,j] = Math.Round(rand.NextDouble()*finishNumber, 1);
        }
    }
    return array;
}

double[,] PrintDoubleArray(double[,] array)
{
    int m =  array.GetLength(0);
    int n =  array.GetLength(1);
    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            Console.Write($"{array[i,j]} ");
        }
    Console.WriteLine();
    }
    return array;
}
//Zadacha47();
