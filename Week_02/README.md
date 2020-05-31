学习笔记

#### HashMap的Java源码小结

##### 	get

​		public V get(Object key)

​		获取对象

​		通过哈希函数（HashMap中是对key的HashCode的处理）计算出key在哈希表对应的位置，然后依次检查该对应位置上的结点，如果是对应的key值，则返回该结点的值。

##### 	put

​		存储对象

​		public V put(K key, V value)

​		通过哈希函数计算出这个key应该存在哈希表所在位置，如果此处为空，则在此新建一个结点存储key-value；如果存在链表，则遍历链表，直到找到存在对应key的结点，更新对应的值；如果不存在对应key的结点，则在链表的末端插入一个结点，存储对象。