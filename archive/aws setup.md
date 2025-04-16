[link to sso](https://hm-sso.awsapps.com/start/#/?tab=accounts)

put in the shell config
```bash
export HENCHMAN_WORK_DIR="~/source/henchman"
alias hm-db-stag-core="AWS_PROFILE=hm-eu-stag $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh stag core-db 38888"
alias hm-db-stag-search="AWS_PROFILE=hm-eu-stag $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh stag search-db 38889"

alias hm-db-eu-prod-core="AWS_PROFILE=hm-eu-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod core-db 38899"
alias hm-db-eu-prod-search="AWS_PROFILE=hm-eu-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod search-db 38898"

alias hm-db-us-prod-core="AWS_PROFILE=hm-us-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod-us core-db 37799"
alias hm-db-us-prod-search="AWS_PROFILE=hm-us-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod-us search-db 37798"

alias hm-db-sa-prod-core="AWS_PROFILE=hm-sa-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod-sa core-db 36699"
alias hm-db-sa-prod-search="AWS_PROFILE=hm-sa-prod $HENCHMAN_WORK_DIR/ops/scripts/bastion_port_forward.sh prod-sa search-db 36698"

alias hm-k8-stag="aws eks update-kubeconfig --name henchman-eks-stag --alias hm-eu-stag --region eu-west-1 --profile hm-eu-stag"
alias hm-k8-eu-prod="aws eks update-kubeconfig --name henchman-eks-prod --alias hm-eu-prod --region eu-west-1 --profile hm-eu-prod"
alias hm-k8-us-prod="aws eks update-kubeconfig --name henchman-eks-use1-prod --alias hm-us-prod --region us-east-1 --profile hm-us-prod"
alias hm-k8-sa-prod="aws eks update-kubeconfig --name henchman-eks-afs1-prod --alias hm-sa-prod --region af-south-1 --profile hm-sa-prod"


```