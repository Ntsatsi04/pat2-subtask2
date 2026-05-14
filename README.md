# pat2-subtask2

 #include <iostream>

using namespace std;

int main()
{
string code[26] =
    {
        ".-", "-...", "-.-.", "-..", ".", "..-.",
        "--.", "....", "..", ".---", "-.-", ".-..",
        "--", "-.", "---", ".--.", "--.-", ".-.",
        "...", "-", "..-", "...-", ".--", "-..-",
        "-.--", "--.."
    };
     cout << "Enter message in English (A-Z characters only): ";
    getline(cin, message);

    // Convert message to uppercase
    transform(message.begin(), message.end(), message.begin(), ::toupper);


    for(int i = 0; i < message.length(); i++)
    {
        char ch = message[i];

        // Check if character is a letter
        if(ch >= 'A' && ch <= 'Z')
        {
         int index = ch - 'A';

            cout << ch << ": " << code[index] << endl;

            morse += code[index] + "   ";
        }
    }

    cout << "Full Morse Message:";
    cout << morse << endl;
    
return 0;}
