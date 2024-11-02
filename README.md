# Percentual-Error
Algoritm to calculate the percentual error of a mesure made in laboratory compared to a theorical value.

n=int(input("Amount of Mesurements"))
teorico=[*range(0,n+1)]
exp=[*range(0,n+1,1)]
erro=[*range(0,n+1,1)]
for i in range (n):
    teorico[i] = float(input("Theoric Values"))
for i in range (n):
    exp[i] = float(input("Experimental Values"))
if len(exp)==len(teorico):
    for i in range (n):
        erro[i]= (exp[i]-teorico[i])*100/teorico[i]
        print("Percentual Error {} = {}%\n".format(i+1,erro[i]))
else:
    print("Invalid amount of mesures, try again")
