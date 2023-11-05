# PFSwChO-lab4

Plik config-quota.yaml ustawia odpowiednie ograniczenia dla namespace lab4

```
kubectl create namespace lab4
kubectl apply -f /home/djkrnl/lab4/tmp/namespace-config.yaml --namespace=lab4
```

![image](https://github.com/W-Sarnowski/PFSwChO-lab4/assets/32043288/8f52eaf4-bf52-457a-b03a-17e1a6120c65)

Następnie przez komendy w terminalu utworzono pody restictednginx i ustawiono ich limity

```
kubectl create deploy resrictednginx --image=nginx -n lab4 --replicas=5
kubectl set resources deploy resrictednginx --requests=memory=64Mi,cpu=125m --limits=memory=256Mi,cpu=250m -n lab4
```

![image](https://github.com/W-Sarnowski/PFSwChO-lab4/assets/32043288/47fb8dc6-975f-437f-9d63-3db15327cdb1)
