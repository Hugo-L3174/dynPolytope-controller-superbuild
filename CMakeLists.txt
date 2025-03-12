AddProject(gram_savitzky_golay
  GITHUB arntanguy/gram_savitzky_golay
  GIT_TAG origin/master
)

AddProject(politopix
  GITHUB_PRIVATE Hugo-L3174/politopix
  GIT_TAG origin/libraryPort 
)

AddProject(DCM_VRPTask
  GITHUB_PRIVATE Hugo-L3174/DCM_VRPTask
  GIT_TAG origin/main
  DEPENDS gram_savitzky_golay 
)

AddProject(mc_dynamic_polytopes
  GITHUB_PRIVATE Hugo-L3174/mc_dynamic_polytopes
  GIT_TAG origin/main
  DEPENDS politopix 
  APT_PACKAGES libqhull-dev
)

AddProject(polytopeController
  GITHUB_PRIVATE Hugo-L3174/polytopeController
  GIT_TAG origin/master
  DEPENDS DCM_VRPTask mc_dynamic_polytopes 
)