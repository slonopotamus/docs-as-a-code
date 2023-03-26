# frozen_string_literal: true

require 'asciidoctor-diagram'
require 'asciidoctor-revealjs'

task :default do
  Asciidoctor.convert_file('index.adoc',
                           backend: 'revealjs',
                           safe: Asciidoctor::SafeMode::UNSAFE,
                           to_dir: 'public',
                           mkdirs: true)
  FileUtils.cp_r('images', 'public') if File.exist?('images')
end
