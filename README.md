# Bitmask
## unique number
    •এক্সঅর(X-OR) অপারেশনের মাধ্যমে রিপিটেট নাম্বার গুলো শুন্য(০) হয়ে যায়। যেমন, ১১,১১,১২,১২ এই নাম্বারগুলোর এক্সঅর(X-OR) অপারেশন করলে উত্তর হবে –    
                                                             
        ৮ ৪ ২ ১
        ১  ০ ১ ১ = ১১
        ১১ বাইনারি – ১ ০ ১ ০  
        ১২ বাইনারি – ১ ০ ০ ০
            ১১ ^ ১১  =  ১ ০ ১ ০ (১১)
                    ^১ ০ ১ ০ (১১)
            ---------------
        		০ ০ ০ ০ ( ১ ^ ১ == ০, ০ ^ ০ = ০, ১ ^ ০ = ১, ০ ^ ১ = ১)
        	
                 ১২ ^ ১২   =  ০
         
        ১১ ^ ১১ ^ ১২ ^ ১২ = ০;
        #include<bits/stdc++.h>
        using namespace std;
        int main(){
            
            cout <<( 11 ^ 10 ^ 11 ^ 9 ^ 10 ^ 5 ^ 9 )<< "\n";
        }


    
