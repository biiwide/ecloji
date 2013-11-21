ecloji
======
So it appears that most Unicode characters can be used in Clojure symbols...  The sky is the limit.

Sample
=====
  => (def 🌀 interleave)
  
  #'user/🌀


  => (🌀 [1 2 3] ["a" "b" "c"])
  
  (1 "a" 2 "b" 3 "c")
