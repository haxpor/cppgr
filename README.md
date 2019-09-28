# cppgr

A simple and convenient bash script to search something (multiple texts) from C++ header source as mostly located at `/usr/include/c++/<version>` but for this the script aims at Gcc version 9.0.

Initially this script helps me on studying internal C++'s STL by quickly grep through the source as seen in various header files. Recommended to also have a copy of [gcc](https://github.com/gcc-mirror/gcc) in case of digging deeper or a certain function is implemented not in header sources.

# Installation

Put `cppgr` script into your `/usr/local/bin/` directory, or clone this repository then symlink the file there.

# Usage

* Search for a single text => `cppgr ostream_iterator`
* Search for multiple texts => 'cppgr iterator class`

Output would be something like this

```
/usr/include/c++/7/backward/hash_map:511:    class insert_iterator<__gnu_cxx::hash_map<_Key, _Tp, _HashFn, 
/usr/include/c++/7/backward/hash_map:553:    class insert_iterator<__gnu_cxx::hash_multimap<_Key, _Tp, _HashFn,
/usr/include/c++/7/backward/hash_set:479:    class insert_iterator<__gnu_cxx::hash_set<_Value, _HashFcn,
/usr/include/c++/7/backward/hash_set:522:    class insert_iterator<__gnu_cxx::hash_multiset<_Value, _HashFcn,
/usr/include/c++/7/bits/hashtable_policy.h:301:  /// Base class for node iterators.
/usr/include/c++/7/bits/hashtable_policy.h:1127:   *  Primary class template _Local_iterator_base.
/usr/include/c++/7/bits/hashtable_policy.h:1129:   *  Base class for local iterators, used to iterate within a bucket
/usr/include/c++/7/bits/stl_raw_storage_iter.h:64:   *  This iterator class lets algorithms store their results into
/usr/include/c++/7/bits/stl_raw_storage_iter.h:68:    class raw_storage_iterator
/usr/include/c++/7/bits/stl_iterator.h:101:    class reverse_iterator
/usr/include/c++/7/bits/stl_iterator.h:455:    class back_insert_iterator
/usr/include/c++/7/bits/stl_iterator.h:547:    class front_insert_iterator
/usr/include/c++/7/bits/stl_iterator.h:642:    class insert_iterator
/usr/include/c++/7/bits/stl_iterator.h:756:  // not a class, e.g. a pointer, into an iterator that is a class.
/usr/include/c++/7/bits/stl_iterator.h:763:    class __normal_iterator
/usr/include/c++/7/bits/stl_iterator.h:1013:    class move_iterator
/usr/include/c++/7/bits/stl_algobase.h:395:    class istreambuf_iterator;
/usr/include/c++/7/bits/stl_algobase.h:398:    class ostreambuf_iterator;
...
```

# License

MIT, Wasin Thonkaew
