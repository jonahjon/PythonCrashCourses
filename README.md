# PythonCrashCourses

Dictonaries:

So everything in Boto3 when you query S3 is given in Dictionaries. So I'm going to do a crash course on them.
Dictionaries are delimited with curly braces and contain a comma separated key-value pairs with each pair tied together by a colon.

'''
Birthdays: = {"John": "16","David": "24"}
>>> Birthdays["John"]
'16'
'''


Copying Dict:
'''
Birthdays = Birthdays.newdict()
newdict = dict(Birthdays)
'''

Updating Dict:
'''
Birthday["Samantha"] = 31
>>> Birthdays
{"John": "16","David": "24", "Samantha": "31"}
'''


Useful trick to loop through all your key values	
'''
Loop integration:
For i in Birthday:
	print("Values of Key " + i + " => " + str(test[i]))
	Values of Key John => 16
	Values of Key David => 24
	Values of Key Samantha => 31
'''

How to get out just keys, or values, or both
'''
Keys method
	>>> Birthday.keys()
	Birthday_keys(['John', 'David', 'Samantha'])

	>>> Birthday.values()
	Birthday_values(['16', '24', '31'])

	>>> Birthday.item()
	Birthday_items([('John,')])
'''


1. Keys
must be unique
immutable type(int,float,string,tuple,bool)
careful with float type as a key(if float have accuracy issue, we may not be able to find out what I am looking)

2. values
any type(immutable and mutable)
can be duplicate
dictionary values can be lists,even other dictionaries

3. No order to keys and values

How to invert Key/Value with pprint:
'''
Birthday = {"John": "16","David": "24"}
BirthdayInvert = {v: k for k,v in Birthday.items()}
>> pprint(BirthdayInvert)

{'16', 'John', '24': 'David'}
'''
