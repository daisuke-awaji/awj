# awj
 awj is a script that enables interactive selection and execution of aws-cli commands by using peco.

 <image>

The origin of the name is "awj" because "aws-cli is supplemented by jq".

## Installation
Place the awj file in `/usr/local/bin` and give execute permission.
Execute the following script and make it readable.
```
$ wget https: //github.com/daisuke-awaji/awj .... \
-P /usr/local/bin

$ chomod 755 /usr/local/bin/awj
```

## Usage

Execute awj, first select the target function.

```
$ awj <Enter>
describe_stacks
describe_stack_url
describe_change_set_url
describe_ec 2
describe_elb
describe_alb
describe_lambda
describe_rds
describe_s 3
describe_logs
describe_aws_batch_jobs
```

You can acquire detailed information on resources provisioned to aws interactively for each selected function.
