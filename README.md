Ruby
====
def ordered_word?(str) 
    i=0;
    letters=str.split("");
    len=letters.length
    while(i<len-1) do
      if(letters[i]>letters[i+1]) 
        return false;
      end
      i+=1;
    end
        return true;
end

ordered_word?("zma")

2)
def encrypt(str)
    letters=str.split("");
    len=letters.length
    i=0;
    count=0;
  
    while(i<len) do
        count=1;
         while(letters[i]==letters[i+1]) do
            i+=1;
            count+=1;
        end
        
        puts letters[i] + ": " + count.to_s;
        i+=1;
    end
end


encrypt("aabbcaaac") ;


3)
def one_off_words(str, word_list)
    string1=str.split("");
    l1=str.length;
    word_list.each do |word|
        l2=word.length;
        count=0;
        i=0;
        if(l1==l2)
            string2=word.split("");
            while(i<=l2) do
                if(string1[i]!=string2[i]) 
                    count+=1;
                end
                i+=1;
            end
            
            if(count<=1)
                puts word;
            end
        end
    end
end

WORDS = ["door", "moot", "boot", "boots"] 
one_off_words("moor", WORDS)
