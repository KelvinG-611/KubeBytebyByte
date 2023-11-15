## Topic 1. kubectl command format

The basic format is `kubectl <action> <resource>`, where `action` can be `create`, `delete`, `get`. You can use kubectl api-resources to get `resource`. 

## Topic 2. Contexts

1. Common commands
View current context: `kubectl config current-context`
List all contexts: `kubectl config get-contexts`
    Understand the output: 
    - CURRENT: Indicates the current active context with an `*`
    - NAME: Context name
    - AUTHINFO: The user credentials used in the context
    - NAMESPACE: The default namespace for the context (if set)
Switch context: `kubectl config use-context [context-name]`

2. What's the relationship between `kubectl config view --minify` and kubeconfig file? 
    it only shows the information related to the current context. This includes the details of the cluster, user, namespace associated with the current context, but exclude the details of other contexts, users in the kubeconfig file.
   
3. What's the relationship between `kubectl config current-context` and kubeconfig file? 
    The current-context that kubectl config current-context shows is the one from the **merged** configuration, with priority given to the current-context in the **last** file listed in the KUBECONFIG variable, if there are conflicting settings.
    
4. What `kubectl config view` does? 
    It will show you the combined version of different kubeconfig files from `echo $KUBECONFIG`
