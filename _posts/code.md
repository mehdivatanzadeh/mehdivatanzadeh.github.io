---
layout: post
title: code post
date: 17.10.03
description: a blog post with some code
tags: formatting code
categories: sample-posts
featured: true
---

this is a cpp code


```markdown
```cpp
    code with cpp
```
```markdown

```cpp
#include<bits/stdc++.h>

using namespace std;

int ans[100001];
queue<int> A;//vard
queue<int> P;//karj
int T = 0;

int main(){
    int s, n, c, d;
    cin >> s >> n;
    for(int i = 0; i < n; i++)ans[i]=-2;
    for(int i = 0; i < n; i++){
        cin >> c >> d;
        while(!A.empty() && P.front() <= c){
            A.pop();
            P.pop();
        }
        if(A.size() == s)ans[i] = -1;
        else{
            T = max(T, c);
            ans[i] = T;
            A.push(c);
            P.push(T + d);
            T += d;
        }
        
    }
    if(n == 0)cout << " ";
    else for(int i = 0; i < n; i++)cout << ans[i] << endl;

}
```