// Задача 25: Напишите цикл, который принимает на вход два числа (A и B) и возводит число A в натуральную степень B.
// 3, 5 -> 243 (3⁵)
// 2, 4 -> 16

int Exponentiation(int numA, int numB){
  int result = 1;
  for(int i=1; i <= numB; i++){
    result = result * numA;
  }
    // int result = Math.Pow(numA, numB);
    return result;
}

  Console.Write("Введите число A: ");
  int numA = Convert.ToInt32(Console.ReadLine());
  Console.Write("Введите число B: ");
  int numB = Convert.ToInt32(Console.ReadLine());

  int exponentiation = Exponentiation(numA, numB);
  Console.WriteLine("Ответ: " + exponentiation);


// Задача 27: Напишите программу, которая принимает на вход число и выдаёт сумму цифр в числе.
// 452 -> 11
// 82 -> 10
// 9012 -> 12
Console.Write("Введите число N: ");
int numN = Convert.ToInt32(Console.ReadLine());

  int SumNumber(int numN){
    
    int counter = Convert.ToString(numN).Length;
    int advance = 0;
    int result = 0;

    for (int i = 0; i < counter; i++){
      advance = numN - numN % 10;
      result = result + (numN - advance);
      numN = numN / 10;
    }
   return result;
  }

int sumNumber = SumNumber(numN);
Console.WriteLine("Сумма цифр в числе: " + sumNumber);