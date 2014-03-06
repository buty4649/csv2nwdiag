csv2nwdiag
==========

CSVファイルからnwdiagファイルを作成

![sample](https://raw.github.com/buty4649/csv2nwdiag/master/sample/sample.png)

使い方
------
```
	$ csv2nwdiag file1.csv file2.csv ... > output.diag
	  or
	$ csv2nwdiag < file1.csv
```

実行例
------
#### 入力
* network1.csv
	
	 ```
	 192.168.1.0/24
	 192.168.1.1,node1
	 192.168.1.2,node2
	 192.168.1.3,node3
	 ```
* network2.csv
	
	 ```
	 192.168.2.0/24
	 192.168.2.1,node1
	 192.168.2.2,node2
	 192.168.2.3,node3
	 192.168.2.4,node4
	 ```

#### 出力
```
nwdiag {
	network network1 {
		address ="192.168.1.0/24";

		node1 [address = "192.168.1.1"];
		node2 [address = "192.168.1.2"];
		node3 [address = "192.168.1.3"];
	}
	network network2 {
		address ="192.168.2.0/24";

		node1 [address = "192.168.2.1"];
		node2 [address = "192.168.2.2"];
		node3 [address = "192.168.2.3"];
		node4 [address = "192.168.2.4"];
	}
}
```

![sample](https://raw.github.com/buty4649/csv2nwdiag/master/sample/sample.png)
