# Sometimes it's a README fix, or something like that - which isn't relevant for
# including in a project's CHANGELOG for example
declared_trivial = github.pr_title.include? "#trivial"

# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "[WIP]"

# Warn when there is a big PR
warn("Big PR") if git.lines_of_code > 500

message "Executed danger file"
php_codesniffer.ignore = "./config,./routes,./vendor,./tests,./database/migrations"
php_codesniffer.filtering = true
php_codesniffer.standard = "PSR12"
php_codesniffer.exec
