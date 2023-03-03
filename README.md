# Ansible Collection - my_own_namespace.yandex_cloud_elk

This collection contains a module that allows you to create a file with specific content.


## Examples

### Check for the presence of the file
    - name: Check for the presence of the file and the default content in it
    ansible.modules.my_own_module:
        path: /tmp/test.txt

### pass in a message and have changed true
    - name: Test with a message and changed output
    ansible.modules.my_own_module:
        path: "/tmp/test.txt"
        content: "hello world"

### fail the module ( folder not a file )
    - name: Test failure of the module
    ansible.modules.my_own_module:
        path: /tmp/



## Options:
    path:
        description: This is full path to file.
        required: true
        type: str
    content:
        description:  content within the file. If it is not found the file will be overwritten with the specified context..
        required: false
        type: str


