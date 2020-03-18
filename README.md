# How to edit Windows registry on Linux

1. First of all, install the tool that will allow you to edit Windows registry from Linux.

    ```bash
    sudo apt install chntpw
    ```

2. Go to the registry Windows folder.

    ```bash
    cd /mnt/sdb0/Windows/System32/config
    ```

3. Depending on which key you want to access you have to chose the right file.

    ```bash
    chntpw -i <FILE>
    ```

4. It will prompt something like this (for `SOFTWARE`, for example).

    ```bash
    chntpw version 1.00 140201, (c) Petter N Hagen
    Hive <SOFTWARE> name (from header): <emRoot\System32\Config\SOFTWARE>
    ROOT KEY at offset: 0x001020 * Subkey indexing type is: 686c <lh>
    File size 89653248 [5580000] bytes, containing 19648 pages (+ 1 headerpage)
    Used for data: 1535227/88876216 blocks/bytes, unused: 34/29512 blocks/bytes.

    <>========<> chntpw Main Interactive Menu <>========<>

    Loaded hives: <SOFTWARE>

      3 - RecoveryConsole settings
      4 - Show product key (DigitalProductID)
          - - -
      9 - Registry editor, now with full write support!
      q - Quit (you will be asked if there is something to save)


    What to do? [1] -> 9
    Simple registry editor. ? for help.
    ```

5. Access whatever the path is.

    ```bash
    cd Microsoft\Windows\CurrentVersion\Policies\System
    ```
