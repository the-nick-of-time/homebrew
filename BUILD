load("@bazel_latex//:latex.bzl", "latex_document")

latex_document(
    name = "homebrew",
    srcs = [
        "BasicRaces.tex",
        "MagicItems.tex",
        "bhan.tex",
        "homebrew.tex",
        "selkie.tex",
        ":addons",
        ":dnd",
    ],
    main = "homebrew.tex",
)

filegroup(
    name = "dnd",
    srcs = [
        ":dnd_dependencies",
        "@dnd_latex//:dndbook",
    ],
)

filegroup(
    name = "dnd_dependencies",
    srcs = ["@bazel_latex//packages:" + pkg for pkg in [
        "babel_english",
        "bookman",
        "cfr-initials",
        "contour",
        "enumitem",
        "etoolbox",
        "expl3",
        "fancyhdr",
        "fontaxes",
        "gensymb",
        "geometry",
        "gillius",
        "hang",
        "initials",
        "kpfonts",
        "l3keys2e",
        "lettrine",
        "microtype",
        "minifp",
        "numprint",
        "ragged2e",
        "tcolorbox",
        "tex-gyre",
        "tikz",
        "titlesec",
        "tocloft",
        "xfrac",
        "xkeyval",
        "xparse",
        "xtemplate",
    ]],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "addons",
    srcs = [
        "@bazel_latex//packages:hyperref",
    ],
    visibility = ["//visibility:private"],
)


