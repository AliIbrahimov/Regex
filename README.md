# Regex
Email and URL Regular Expressions

This repository contains regular expressions for validating email addresses and URLs. The regular expressions are provided in separate text files.

Files:
- emailRegex.txt: Contains a regular expression pattern for validating email addresses.
- urlRegex.txt Contains a regular expression pattern for validating URLs.

Usage:
1. Clone the repository or download the text files directly.
2. Open the desired text file to access the regular expression pattern.
3. Copy the regular expression and use it in your preferred programming language or text editor to validate email addresses or URLs.

Example Usage (C#):

```csharp
using System;
using System.Text.RegularExpressions;

class Program
{
    static void Main()
    {
        string emailPattern = @"^([a-zA-Z0-9]+([\\._\\-]{1})?){1,}[\\w]\\@{1}([a-zA-Z]+([\\.]{1})?){1,}([a-zA-Z])\\.[a-zA-Z]+$";
        string urlPattern = @"^(https?|ftp)://[^\s/$.?#].[^\s]*$";

        string email = "example@example.com";
        if (Regex.IsMatch(email, emailPattern))
        {
            Console.WriteLine("Valid email address");
        }
        else
        {
            Console.WriteLine("Invalid email address");
        }

        string url = "http://www.example.com";
        if (Regex.IsMatch(url, urlPattern))
        {
            Console.WriteLine("Valid URL");
        }
        else
        {
            Console.WriteLine("Invalid URL");
        }
    }
}
