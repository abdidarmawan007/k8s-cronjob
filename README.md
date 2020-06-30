# run cronjobs in k8s

kubectl apply -f cronjobs.yaml


kubectl get cronjob -n staging
```
NAME                  SCHEDULE      SUSPEND   ACTIVE   LAST SCHEDULE   AGE
staging-cron-sender   */3 * * * *   False     1        2m15s           3m33s
```

kubectl get job -n staging
```
NAME                             COMPLETIONS   DURATION   AGE
staging-cron-sender-1593493740   1/1           2s         40s
```
