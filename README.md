ecloji
======
So it appears that most Unicode characters can be used in Clojure symbols...  The sky is the limit.

Samples
=====
  => (def 🌀 interleave)
  
  #'user/🌀


  => (🌀 [1 2 3] ["a" "b" "c"])
  
  (1 "a" 2 "b" 3 "c")


  => (defrecord 👤 [🏠 🏫 🏢 📞 📱])
  
  user.👤

  => (map->👤 {:🏠 "123 Washington Ave." :🏫 "UofM Twin Cities" :🏢 "CoCo Minneapolis" :📞 "867-5309" :📱 "555-5555"})

  #user.👤{:🏠 "123 Washington Ave.", :🏫 "UofM Twin Cities", :🏢 "CoCo Minneapolis", :📞 "867-5309", :📱 "555-5555"}

  => (type 👤)

  java.lang.Class

  => (.getName 👤)

  "user.👤"
