ecloji
======
So it appears that most Unicode characters can be used in Clojure symbols...  The sky is the limit.

### Samples

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


### Also of Interest
Unicode has many different groups of "digit" (base 10) glyphs.  Java's Character class recognizes many
of these as digits:

    assertTrue( Character.isDigit('၅') );

Additionally, the Number classes appear to be able to parse them:

    assertEquals( 1111, Long.valueOf("١٢٣") );

Even more fun is that Java doesn't even care if they are all from the same group of digits:

    assertEquals( 12121212, Long.valueOf("١٢১২၁၂12") );
