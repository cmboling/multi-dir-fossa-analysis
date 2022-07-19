# multi-dir-fossa-analysis

### About this repository

This is an example of using the FOSSA CLI within a GitHub Action workflow. When dealing with a monorepo, you can apply a `.fossa.yml` to each applicable directory that you'd like FOSSA to scan.
This is a granular way of doing it (manually `.fossa.yml` to each applicable directory, but there are some cool tricks to dynamically create the `.fossa.yml` in the Action workflow to reduce/simplify the implementation. 

#### Why would you want to do this?

Cut down on analysis time.

### Suggestions

Run `fossa list-targets` to figure out which targets FOSSA is able to analyse. Once you have that list, create the `.fossa.yml`. See [fossa.yml documentation](https://github.com/fossas/fossa-cli/blob/master/docs/references/files/fossa-yml.md) for reference.

### Expected output

Each subdirectory is its own project in FOSSA.

![image](https://user-images.githubusercontent.com/1427948/179844466-273de9c4-b003-4237-b14f-e23711620226.png)
