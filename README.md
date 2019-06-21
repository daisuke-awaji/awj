# awj
 awj is a script that enables interactive selection and execution of aws-cli commands by using peco.

 ![ec2.gif](gif/ec2.gif)

The origin of the name is "awj" because "aws-cli is supplemented by jq".

## Installation

### Required commands
- jq
  ```
  # Install jq
  $ yum install jq
  ```
- peco
  ```
  # Install peco
  $ cd /usr/local/bin
  $ wget https://github.com/peco/peco/releases/download/v0.2.9/peco_linux_amd64.tar.gz
  $ tar -C /usr/local/bin -xzf peco_linux_amd64.tar.gz
  $ sudo mv ./peco_linux_amd64/peco /usr/local/bin/
  $ chmod 755 /usr/local/bin/peco
  $ sudo rm -rf /usr/local/bin/peco_linux_amd64.tar.gz
  ```

### Install awj

1. Add /usr/local/bin to PATH environment on OS.
1. Place the awj file in `/usr/local/bin` and give execute permission.
1. Execute the following script and make it readable.
  ```
  # Install awj
  $ wget https://raw.githubusercontent.com/daisuke-awaji/awj/master/awj \
         -P /usr/local/bin
  $ chmod 755 /usr/local/bin/awj
  ```


## Usage

Execute awj, first select the target function.

```
$ awj <Enter>
describe_stacks
describe_stack_url
describe_change_set_url
describe_ec2
describe_elb
describe_alb
describe_lambda
describe_rds
describe_s 3
describe_logs
describe_aws_batch_jobs
```

You can acquire detailed information on resources provisioned to aws interactively for each selected function.
It is useful to register the awj command in the alias command a.

In the following example, after deploying the resource of lambda with aws cloudformation, it is a flow to confirm with aws console whether the stack was executed normally.

 ![ec2.gif](gif/stack.gif)
