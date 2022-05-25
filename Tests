using System;

namespace ConsoleApp1
{
    public class Program
    {
        static string[] tests = new string[]
        {
            "Ебаааааал тебя в пизззззду мр....азь ебливая,           подойди сюда, х. у     .епутало шЕБУТной ты. Ебут тебя в жопу как шлюхXXу...",
            "3b4l Тебя w ni3dy mRa3b эbjluva9, подойди сюда, h/u3путало ш3БУТной ты. йеьym тебя в жопу как vvlyoxu...",
            "застраХУЙ свою wlyoNdру",
            "хер тебе, а не херсон!"
        };

        static char[] replacers = new char[]
        {
            '*', '#', '@', '&'
        };

        public static void Main()
        {
            StringFilter sf = new StringFilter();

            Random r = new Random();

            Console.WriteLine($"Всего слов загружено: {sf.FilterWords.Count}\n");

            Console.WriteLine("Ровняем с концов и убираем лишние пробелы и символы: \n");

            for (int i = 0; i < tests.Length; i++)
            {
                tests[i] = StringFilter.Beatify(tests[i], true, true, true);

                Console.WriteLine(tests[i]);
            }

            Console.WriteLine("\nПроверяя на исключения: \n");

            foreach (var test in tests)
                Console.WriteLine(sf.Process(test, true, false, replacers[r.Next(0, replacers.Length)]));

            Console.WriteLine("\nНе проверяя на исключения: \n");

            foreach (var test in tests)
                Console.WriteLine(sf.Process(test, false, false, replacers[r.Next(0, replacers.Length)]));

            Console.WriteLine("\nПроверяем исключения и скрываем матерные слова целиком: \n");

            foreach (var test in tests)
                Console.WriteLine(sf.Process(test, true, true, replacers[r.Next(0, replacers.Length)]));
        }
    }
}
