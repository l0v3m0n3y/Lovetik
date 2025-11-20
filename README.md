# Lovetik
api for lovetik.com free tiktok download video site
# main
```cpp
#include "Lovetik.h"
#include <iostream>

int main() {
   Lovetik api;

    auto video = api.search_video("https://www.tiktok.com/video/link").then([](json::value result) {
        std::cout << result<< std::endl;
    });
    video.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
