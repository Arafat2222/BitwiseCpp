# [https://www.geeksforgeeks.org/bitwise-hacks-for-competitive-programming/]
# Bitmask
## unique number
    •এক্সঅর(X-OR) অপারেশনের মাধ্যমে রিপিটেট নাম্বার গুলো শুন্য(০) হয়ে যায়। যেমন, ১১,১১,১২,১২ এই নাম্বারগুলোর এক্সঅর(X-OR) অপারেশন করলে উত্তর হবে –    
                                                             
        ৮ ৪ ২ ১
        ১  ০ ১ ১ = ১১
        ১১ বাইনারি – ১ ০ ১ ০  
        ১২ বাইনারি – ১ ০ ০ ০
            ১১ ^ ১১  =  ১ ০ ১ ০ (১১)
                      ^ ১ ০ ১ ০ (১১)
                        ---------------
        		    ০ ০ ০ ০ ( ১ ^ ১ == ০, ০ ^ ০ = ০, ১ ^ ০ = ১, ০ ^ ১ = ১)
        	
                 ১২ ^ ১২   =  ০
         
        ১১ ^ ১১ ^ ১২ ^ ১২ = ০;
        টাইম কম্পেক্সলিটি o(n).
        #include<bits/stdc++.h>
        using namespace std;
        int main(){
            
            cout <<( 11 ^ 10 ^ 11 ^ 9 ^ 10 ^ 5 ^ 9 )<< "\n";
        }

## Odd-Even
    
    •অ্যন্ড (AND &) অপারেশনের মাধ্যামে জোড়-বিজোড় সংখ্যা নির্ণয় করা যায়-
    ধরি, একটি সংখ্যা ৭। ৭ এর বাইনারি হলো – ১ ১ ১ 
    (৭&১) = ১ ১ ১
    	০ ০ ১
    	------------
    	০ ০ ১
    তাই,(৭&১) == ১ হয় তাহলে নাম্বারটি বিজোড়।
    
    এবার একটি জোড় সংখ্যার উদাহরণ দেওয়া যাক,
    						১২ এর বাইনারি – ১ ১ ০ ০
    						১২ & ১	= ১ ১ ০ ০
    							& ০ ০ ০ ১
    					            --------------------
    							০ ০ ০ ০
    
    
    ধরা যাক, n একটি নাম্বার। যদি (n & ১) হয় তবে জোড় না হলে বিজোড়।

											
 	#include<bits/stdc++.h>
    using namespace std;
    int main(){
        int n;
        cin >> n;
        if(n&1){
            cout << "Odd\n";
        }
        else{
            cout << "Even\n";
        }
    }
     					



    
