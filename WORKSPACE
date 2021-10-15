load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

# D&D template
new_git_repository(
    name = "dnd_latex",
    build_file = "@//tools/latex:dndbook.BUILD.bazel",
    commit = "2c94ab97952b8285bbbc932ccd507cbcd931ef82",
    remote = "https://github.com/rpgtex/DND-5e-LaTeX-Template.git",
    shallow_since = "1625601769 +0200",
)

# Latex rules
http_archive(
    name = "bazel_latex",
    patches = ["//:latex_packages.patch"],
    sha256 = "4af7e8bc134e8b24d5f4b01b06d150d096b1698bdcbd38683cd18ee01af39fa5",
    strip_prefix = "bazel-latex-1.1",
    url = "https://github.com/ProdriveTechnologies/bazel-latex/archive/v1.1.tar.gz",
)

