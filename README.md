# FileQuery
	// Query a file on your system

	var fileName = @"C:\Work\Myfile.cs";

            var fileQuery = new FileQuery.QueryFile();

	var check = fileQuery.Query(fileName);

            foreach (var item in check)
            {
                Console.WriteLine(item);
            }


	// Convert to JSON
	var json = fileQuery.ToJson();

            Console.WriteLine(json);
		

            // Query specific TEXT in the file..
	var checkBool = fileQuery.Query(fileName).Select(a => a.IndexOf("N/A") > -1).ToList();

            foreach (var item in checkBool)
            {
                        Console.WriteLine(item);
            }
