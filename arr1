#include <iostream>
class Array
{
    int* mas;
    uint16_t size;
public:
    Array(uint16_t sizeP = 10) :size{ sizeP }, mas{ new int[sizeP] }{fill();}
    Array(const Array& arr) :size{ arr.size }, mas{ new int[arr.size] }
    {
        for (int i{ 0 }; i < size; ++i) {
            mas[i] = arr.mas[i];
        }
    }
    void fill()
    {
        for(int i = 0;i<size;++i){
            mas[i] = rand() % 100;
        }
    }
    void setsize(uint16_t siz)
    {
        size = siz;
        int* masP{ new int[siz] };
        for (int i = 0; i < siz; ++i) {
            if (size <= i) {
                masP[i] = 0;
            }
            else
            {
                masP[i] = mas[i];
            }
        }
        delete[]mas;
        mas = masP;
    }
 
    int getsize()
    {
        return size;
    }

    int getvalue(int index,int value)
    {
        if (size > index && index >= 0)
        {
            mas[index] = value;
        }
        return 0;
    }
    void dismas()
    {
        for (int i = 0; i < size; ++i) {
            std::cout << mas[i] << ", ";
        }
        std::cout << mas[size - 1] << std::endl;
    }
    void sortmas() {
        int a = 0;
        for (int i = 0; i < size; ++i) {
            for (int j = i; j < size; ++i) {
                if (mas[i] > mas[j])
                {
                    a = mas[i];
                    mas[i] = mas[j];
                    mas[j] = a;
                    
                    
                }           
            }
        }
    }
    int maxmas() {
        int a=mas[0];
        for (int i = 1; i < size; ++i) {
            if(a<mas[i])
            {
                a = mas[i];
            }
            return a;
        }
    }
    int minmas() {
        int a = mas[0];
        for (int i = 1; i < size; ++i) {
            if (a > mas[i])
            {
                a = mas[i];
            }
            return a;
        }
    }
    ~Array()
    {
        delete[]mas;
    }
};
int main()
{
    Array bar1;
    bar1.getsize();
    bar1.getvalue(4,5);
    bar1.dismas();
    Array bar2;
    bar2.setsize(20);
    bar2.sortmas();
    bar2.dismas();
}
