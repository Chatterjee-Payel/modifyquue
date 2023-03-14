# modifyquue
queue<int> modifyQueue(queue<int> q, int k) {
    // add code here.
    queue<int>ans;
    stack<int>s;
    while(q.size()>0 && k>0)
    {
        s.push(q.front());
        q.pop();
        k--;
    }
    while(s.size()>0)
    {
        ans.push(s.top());
        s.pop();
        
    }
    while(q.size()>0)
    {
        ans.push(q.front());
        q.pop();
    }
    return ans;
};

