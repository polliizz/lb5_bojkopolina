# lb5_bojkopolina
#include <iostream>
using namespace std;

int main() {
    const int N = 3;
    int matrix[3][3] = {
        {7, 9, 3},
        {0, 3, 0},
        {1, 2, 0}
    };
    cout << "Матриця: \n";
    for (int i = 0; i < N; i++) {
        for (int j = 0; j < N; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << '\n';
    }
    int povorot[N][N];
    for (int i = 0; i < N; i++) {
        for (int j = 0; j < N; j++) {
            povorot[j][N - i - 1] = matrix[i][j];
        }
    }
    cout << '\n' << "Поворот на 90: "<< '\n';
    for (int i = 0; i < N; i++) {
        for (int j = 0; j < N; j++) {
            cout << povorot[i][j] << " ";
        }
        cout << '\n';
    }
}
