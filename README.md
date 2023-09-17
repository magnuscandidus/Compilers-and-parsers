# Compilers-and-parsers
#include <bits/stdc++.h>

using namespace std;
int main() {
	int t; cin>>t;
	while(t--){
	    string s; cin>>s;
	    int sum = 0,ans = 0;
	    stack<char> stack;
	    for(int i = 0; i < s.size(); i++){
	        char ch = s[i];
	        if(stack.empty()){
	            stack.push(ch);
	        }
	        else{
	            if(stack.top() == '<' && ch == '>'){
	                stack.pop();
	            }
	            else{
	                stack.push(ch);
	            }
	        }
	        if(stack.empty()) ans = i+1;
	    }
	    cout<<ans<<endl;
	}
}
