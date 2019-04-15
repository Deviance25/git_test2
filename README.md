# stepik 3.4

l, d = [], {}
a, b, c, cnt1, cnt2, cnt3 = 0, 0, 0, 0, 0, 0
with open("test.txt", 'r') as s:
    for i in s:
        l.extend([i.strip().split(';')])
for i in l:
    d[i[0]] = i[1:]
for i in d:
    sum = 0
    cnt = 0
    for j in d.get(i):
       cnt += 1
       sum += int(j)
    print(sum/cnt)
for i in d:
    k = []
    for j in d.get(i):
        k.append(int(j))
    for h in k[:-2]:
            a += h
            cnt1 += 1
    for h in k[1:-1]:
            b += h
            cnt2 += 1
    for h in k[2:]:
            c += h
            cnt3 += 1
print(a/cnt1, b/cnt2, c/cnt3)

