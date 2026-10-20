# Claude reviews

Repository owners and members can request a pull request review by commenting
`@claude`. The workflow uses `prompts/code-review.md` and posts the review as a
pull request comment. Add instructions after `@claude` to use interactive mode
with the triggering comment and conversation context instead.

Reviews use Claude Sonnet 4.6 through the US cross-region Bedrock inference
profile in `us-west-2`. Configure the model with the pinned action's
`claude_args: --model` input; `anthropic_model` is not supported. The workflow
has a ten-minute job timeout. The inference role must permit invocation of the
profile and its destination models.

Comment-triggered workflows use the default branch's workflow definition.
End-to-end verification of workflow changes requires merging them before
requesting another review.
