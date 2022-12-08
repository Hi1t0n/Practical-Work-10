# Practical-Work-10
# Проверка
def F():
    i = 0
    while i > len(_message):
        if _message[i] == e[i]:
            continue
        else:
            return False
    return True


# Хэш Функция
def hashFun(s):
    num = 1
    for c in s:
        if int(c) != 0:
            num *= int(c)
    return num

# Шифровка
def encr(me):
    return (me ** e) % n

# Расшифровка
def decr(me):
    return (me ** d) % n

p = 13
q = 7
e = 5
d = 29
n = p * q
Fe = (p-1)*(q-1)


message = ['212', '398', '00']
print("Исходное сообщение: 21239800")
_message = []
t = []
_e = []

for me in message:
    temp = encr(hashFun(me))
    _message.append(hashFun(me))
    t.append(temp)

for me in t:
    temp = decr(me)
    _e.append(temp)

for i in t:
    print(i, end='')
print('')

for i in _e:
    print(i, end='')
print('')

print("Верно?", F())
