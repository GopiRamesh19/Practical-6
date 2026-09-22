#include <iostream>
#include <vector>
#include <climits>
using namespace std;

int Matrix_Mul(vector<int> p)
{
    int n = p.size();

    vector<vector<int>> m(n, vector<int>(n, 0));

    for (int t = 2; t < n; t++)
    {
        for (int i = 0; i < n - t; i++)
        {
            int j = i + t;

            m[i][j] = INT_MAX;

            for (int k = i + 1; k < j; k++)
            {
                int cost = m[i][k]
                         + m[k][j]
                         + p[i] * p[k] * p[j];

                if (cost < m[i][j])
                {
                    m[i][j] = cost;
                }
            }
        }
    }

    return m[0][n - 1];
}

int main()
{
   
    vector<int> p = {10, 20, 30, 40, 30};

    cout << "Minimum number of multiplications = "
         << Matrix_Mul(p) << endl;

    return 0;
}     
