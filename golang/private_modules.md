### Working with private modules

In order to use private modules for which Go should not use GOPROXY and GOSUMDB, 

should be able to download access packages hosted on private repos or repos,

other than github we can set the GOPRIVATE env variable

`
GOPRIVATE=gitlab.com/sample-project-group/*,bitbucket.com/sample-group/*
`

This is a regex so we can put either the exact path or a regex with , seperated.

Also git might need to be changed in order to use ssh instead of https.

This is the command for bibucket repos:

`
git config --global url."git@{{gitlab.com}}:".insteadOf "https://gitlab.com/"
`

