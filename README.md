# FileQuery
Query a file on your system

var fileName = @"C:\Temp\Work\NA_Log.txt";

            var fileQuery = new FileQuery.QueryFile();

            var check = fileQuery.Query(fileName).Select(a => a.IndexOf("N/A") > -1).ToList();

            foreach (var item in check)
            {
                Console.WriteLine(item);
            }

            Console.ReadLine();
