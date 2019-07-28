## Tree-Generator
Help problem setters to generate a variety of trees.

You can generate different trees with few functions or even a string, and customize the output function or the random function.

### How to use?

Please read the [GUIDEBOOK](/GUIDEBOOK.md).

### Demo

```cpp
#include "treegenerator.h"

using namespace std;
using namespace tree_generator_by_ouuan;

void myOutputEdge(ostream& os, int u, int fa)
{
    os << u << ' ' << fa << ' ' << randint(1, 10) << endl;
}

int main()
{
    cout << Tree("ch20,0al5,1,20") << endl;
    cout << Tree("bi30,0ch10,20fl10,40") << endl;

    Tree t("cp20,4,0");
    t.complete(20, 4, 0);
    t.shuffleNodes();
    t.shuffleEdges();
    outputEdge = myOutputEdge;
    cout << t << endl;

    return 0;
}
```