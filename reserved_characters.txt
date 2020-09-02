and	exec	not
assert	finally	or
break	for	pass
class	from	print
continue	global	raise
def	if	return
del	import	try
elif	in	while
else	is	with
except	lambda	yield

1.exec 
exec(expression) 执行expression语句，expression为字符串
exp=" print('hello world')" exec(exp)
2.assert（断言）raise(显式的引发异常)
assert exp或者 assert exp ,arguments (exp返回一个布尔值)
等价于 
if not exp:
  raise AssertionError/raise AssertionError(arguments) （arguments为字符串，是异常提示）
3.finally
try: except:finally: 连用，不同是否触发异常，跳出try的时候都要执行finally后面的语句
4.del
del删除的是变量，不是内存对应数据，它和C语言的free和C++的delete不同。例如：
    a=1       # 对象 1 被 变量a引用，对象1的引用计数器为1  
    b=a       # 对象1 被变量b引用，对象1的引用计数器加1  
    c=a       #1对象1 被变量c引用，对象1的引用计数器加1  
    del a     #删除变量a，解除a对1的引用  
    del b     #删除变量b，解除b对1的引用  
    print(c)  #最终变量c仍然引用1  
5.with
with open('test.txt','r') as item:
  for line in item:
    print(line)
