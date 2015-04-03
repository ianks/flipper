# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard 'bundler' do
  watch('Gemfile')
  watch(/^.+\.gemspec/)
end

rspec_options = {
  :all_after_pass => false,
  :all_on_start   => false,
  :failed_mode    => :keep,
  :cmd            => "bundle exec rspec",
}

guard 'rspec', rspec_options do
  watch(%r{^spec/.+_spec\.rb$}) { "spec" }
  watch(%r{^lib/(.+)\.rb$}) { "spec" }
  watch(%r{shared_adapter_specs\.rb$}) { "spec" }
  watch('spec/helper.rb') { "spec" }
end
