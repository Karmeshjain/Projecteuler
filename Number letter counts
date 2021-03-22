
#include <iostream>
#include <string>
using namespace std;
string convert(unsigned long long x)
{
#ifdef ORIGINAL
  const std::string Gap = " And "; // British
  const std::string ConnectTensAndOnes = "-";
#else
  const std::string Gap = " ";
  const std::string ConnectTensAndOnes = " ";
#endif


  switch(x)
  {
    case  0: return "Zero";
    case  1: return "One";
    case  2: return "Two";
    case  3: return "Three";
    case  4: return "Four";
    case  5: return "Five";
    case  6: return "Six";
    case  7: return "Seven";
    case  8: return "Eight";
    case  9: return "Nine";
    case 10: return "Ten";
    case 11: return "Eleven";
    case 12: return "Twelve";
    case 13: return "Thirteen";
    case 14: return "Fourteen";
    case 15: return "Fifteen";
    case 16: return "Sixteen";
    case 17: return "Seventeen";
    case 18: return "Eighteen";
    case 19: return "Nineteen";
    default: break;
  }

  if (x >= 20 && x < 100)
  {
    auto ones = x % 10;
    auto tens = x / 10;
    auto strOnes = (ones != 0) ? ConnectTensAndOnes + convert(ones) : "";
    switch (tens)
    {
      case 2: return "Twenty"  + strOnes;
      case 3: return "Thirty"  + strOnes;
      case 4: return "Forty"   + strOnes; 
      case 5: return "Fifty"   + strOnes;
      case 6: return "Sixty"   + strOnes;
      case 7: return "Seventy" + strOnes;
      case 8: return "Eighty"  + strOnes;
      case 9: return "Ninety"  + strOnes;
      default: break;
    }
  }

  if (x >= 100 && x < 1000)
  {
    auto onesAndTens = x % 100;
    auto hundreds    = x / 100;
    auto strOnesAndTens = (onesAndTens != 0) ? Gap + convert(onesAndTens) : "";
    return convert(hundreds) + " Hundred" + strOnesAndTens;
  }

  return "?";
}

int main()
{


    unsigned long long x;
    std::cin >> x;
    std::cout << convert(x) << std::endl;

  return 0;
}
