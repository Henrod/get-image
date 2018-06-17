if [ -z $3 ]; then
  kubectl --context $1 -n $2 get deploy -o json | jq -r '.items[] | (.metadata.name + ": " + .spec.template.spec.containers[].image)'
else
  kubectl --context $1 -n $2 get po $3 -o json | jq -r .spec.containers[].image
fi
