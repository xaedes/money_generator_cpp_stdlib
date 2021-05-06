# money_generator_cpp_stdlib

```c++
// Infinite Money Generator via C++ standard library
// MIT License
#include <iostream>
#include <sstream>
#include <iomanip>

int main()
{
    const std::string infinite_money = "$1,000,000,000.00";
    const auto locale = std::locale("en_US.UTF-8");
    std::cout.imbue(locale);
    std::cout << std::showbase;
    while(true)
    {
        long double money; 
        std::istringstream money_stream(infinite_money);
        money_stream.imbue(locale);
        money_stream >> std::get_money(money);
        std::cout << std::put_money(money, true) << std::endl;
    };
}
```
