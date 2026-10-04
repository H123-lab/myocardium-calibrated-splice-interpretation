# Append the diagnostic harmonization boundary declaration to your master workflow audit file
cat << 'EOF' >> analysis_workflow.md

### Diagnostic Label Adjudication Framework Boundary
Diagnostic labels were taken directly from the originating public studies or source registries and harmonized to the prespecified diagnostic categories used in the present analysis; no independent diagnostic re-adjudication was performed. This ensures complete traceability to the public source metadata definitions.
EOF

# Stage, commit, and securely synchronize the update with GitHub
git add analysis_workflow.md
git commit -m "docs(workflow): document diagnostic label harmonization boundary to prevent adjudication queries"
git push origin main
