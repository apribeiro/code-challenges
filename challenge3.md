```
var result = [];
var dictionary = {
	'277': 'app',
	'27753': 'apple',
	'227': ['bar', 'car'],
	'344': ['dig', 'fig'],
	'364': 'dog',
	'7223': 'race',
	'733': 'red',
	'763': 'rod',
	'92837': 'water'
};
    
for (var key in dictionary) {
	if (S.length <= key.length) {
		if (key.startsWith(S))
			result.push(dictionary[key]);
	} else {
		if (S.startsWith(key))
			result.push(dictionary[key]);
	}
}

return result.join();
```
