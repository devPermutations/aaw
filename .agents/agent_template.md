<!-- Agent Template - {AGENT_NAME} Agent -->
<!-- Version: {VERSION} -->
<!-- Created: {CREATED_DATE} -->
<!-- Updated: {UPDATED_DATE} -->
<!-- Author: {AUTHOR} -->
<!-- Purpose: {PURPOSE} -->
<!-- Dependencies: {DEPENDENCIES} -->
<!-- Phase: {PHASE} -->
<!-- Artifacts Produced: {ARTIFACTS_PRODUCED} -->
<!-- Dependencies: {UPSTREAM_AGENTS} -->

<agent>
    <meta>
        <version>{VERSION}</version>
        <created>{CREATED_DATE}</created>
        <updated>{UPDATED_DATE}</updated>
        <author>{AUTHOR}</author>
        <purpose>{PURPOSE}</purpose>
        <description>
            {DESCRIPTION}
        </description>
        <phase>{PHASE}</phase>
        <specialization>{SPECIALIZATION}</specialization>
        <capabilities>
            {CAPABILITIES_LIST}
        </capabilities>
        <core_competencies>
            {CORE_COMPETENCIES_LIST}
        </core_competencies>
        <dependencies>
            {DEPENDENCIES_LIST}
        </dependencies>
        <workflow>
            <name>{WORKFLOW_NAME}</name>
            <role>{AGENT_ROLE}</role>
        </workflow>
        <artifacts>
            <produced>
                {ARTIFACTS_PRODUCED_LIST}
            </produced>
            <consumed>
                {ARTIFACTS_CONSUMED_LIST}
            </consumed>
        </artifacts>
        <integration_points>
            <upstream_agents>
                {UPSTREAM_AGENTS_LIST}
            </upstream_agents>
            <downstream_agents>
                {DOWNSTREAM_AGENTS_LIST}
            </downstream_agents>
        </integration_points>
    </meta>
    <ecosystem_awareness>
        <template_foundation>{TEMPLATE_FOUNDATION}</template_foundation>
        <workflow_documentation>{WORKFLOW_DOCUMENTATION}</workflow_documentation>
        <artifact_mapping>{ARTIFACT_MAPPING}</artifact_mapping>
        <agent_organization>
            <planning_phase>
                <directory>{PLANNING_PHASE_DIRECTORY}</directory>
                <agents>
                    {PLANNING_PHASE_AGENTS_XML}
                </agents>
            </planning_phase>
            <development_phase>
                <directory>{DEVELOPMENT_PHASE_DIRECTORY}</directory>
                <agents>
                    {DEVELOPMENT_PHASE_AGENTS_XML}
                </agents>
            </development_phase>
        </agent_organization>
    </ecosystem_awareness>
    <capabilities>
        {CAPABILITIES_XML}
    </capabilities>
    <working_protocol>
        <initial_engagement>
            {INITIAL_ENGAGEMENT_XML}
        </initial_engagement>
        <clarifying_questions_approach>
            {CLARIFYING_QUESTIONS_XML}
        </clarifying_questions_approach>
        <agent_components>
            {AGENT_COMPONENTS_XML}
        </agent_components>
    </working_protocol>
    <design_principles>
        {DESIGN_PRINCIPLES_XML}
    </design_principles>
    <agent_patterns>
        <planning_phase_patterns>
            {PLANNING_PHASE_PATTERNS_XML}
        </planning_phase_patterns>
        <development_phase_patterns>
            {DEVELOPMENT_PHASE_PATTERNS_XML}
        </development_phase_patterns>
        <cross_cutting_patterns>
            {CROSS_CUTTING_PATTERNS_XML}
        </cross_cutting_patterns>
    </agent_patterns>

    <quality_assurance>
        {QUALITY_ASSURANCE_XML}
    </quality_assurance>

    <iterative_refinement>
        {ITERATIVE_REFINEMENT_XML}
    </iterative_refinement>

    <output_standards>
        <file_organization>
            {FILE_ORGANIZATION_XML}
        </file_organization>
        <metadata_requirements>
            {METADATA_REQUIREMENTS_XML}
        </metadata_requirements>
        <documentation_updates>
            {DOCUMENTATION_UPDATES_XML}
        </documentation_updates>
    </output_standards>

    <communication_style>
        {COMMUNICATION_STYLE_XML}
    </communication_style>

    <workflow_templates>
        <planning_phase_template>
            {PLANNING_PHASE_TEMPLATE_XML}
        </planning_phase_template>
        <development_phase_template>
            {DEVELOPMENT_PHASE_TEMPLATE_XML}
        </development_phase_template>
    </workflow_templates>

    <quality_checklist>
        {QUALITY_CHECKLIST_XML}
    </quality_checklist>

    <meta_agent_tracking>
        {META_AGENT_TRACKING_XML}
    </meta_agent_tracking>

    <instructions>
        {INSTRUCTIONS_XML}
    </instructions>

    <progress_tracking>
        <files_to_update>
            {PROGRESS_FILES_XML}
        </files_to_update>
        <update_triggers>
            {UPDATE_TRIGGERS_XML}
        </update_triggers>
        <format_requirements>
            {PROGRESS_FORMAT_XML}
        </format_requirements>
    </progress_tracking>

    <quality_standards>
        <pre_completion_checks>
            {QUALITY_CHECKS_XML}
        </pre_completion_checks>
        <review_criteria>
            {REVIEW_CRITERIA_XML}
        </review_criteria>
        <error_handling_procedures>
            {ERROR_HANDLING_PROCEDURES_XML}
        </error_handling_procedures>
    </quality_standards>

    <input_schema>
        {INPUT_SCHEMA_XML}
    </input_schema>

    <output_schema>
        {OUTPUT_SCHEMA_XML}
    </output_schema>

    <error_handling>
        <strategy>{ERROR_STRATEGY}</strategy>
        <fallback_actions>
            {FALLBACK_ACTIONS}
        </fallback_actions>
        <escalation_paths>
            {ESCALATION_PATHS_XML}
        </escalation_paths>
    </error_handling>

    <metrics>
        <performance_indicators>
            {PERFORMANCE_INDICATORS}
        </performance_indicators>
        <quality_measures>
            {QUALITY_MEASURES}
        </quality_measures>
        <success_criteria>
            {SUCCESS_CRITERIA_XML}
        </success_criteria>
    </metrics>
</agent>
