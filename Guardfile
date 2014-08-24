cmd = {
    cmd: 'bundle exec rspec', 
    spec_paths: ['spec'], 
    failed_mode: :focus,
    all_after_pass: false,
    all_on_start: true, 
    launchy: /tmp/spec_results.html,     
    notification: true
}

guard :rspec, cmd: cmd do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec" }
end

