project('com.github.donadigo.appeditor', ['vala', 'c'],
        version: '0.0.1')

i18n = import('i18n')

conf = configuration_data()
conf.set_quoted('GETTEXT_PACKAGE', meson.project_name())
configure_file(output: 'config.h', configuration: conf)
config_h_dir = include_directories('.')

c_args = [
  '-include', 'config.h'
]

deps = [
  dependency('granite'),
  dependency('gtk+-3.0'),
  dependency('gee-0.8')
]

executable(
    meson.project_name(),
    'src/Application.vala',
    'src/MainWindow.vala',
    'src/Sidebar.vala',
    'src/AppItem.vala',
    'src/CategoryItem.vala',
    'src/IconButton.vala',
    'src/SettingBox.vala',
    'src/PersistentPlaceholderEntry.vala',
    'src/FieldEntry.vala',
    'src/CategoryComboBox.vala',
    'src/AppInfoViewStack.vala',
    'src/AppInfoView.vala',
    'src/MessageDialog.vala',
    'src/AppDirectoryScanner.vala',
    'src/DesktopApp.vala',
    'src/DesktopAppManager.vala',
    'src/AppInfoViewSaver.vala',
    'src/IconListBox.vala',
    'src/IconChooserDialog.vala',
    'src/IconRow.vala',
    'src/Constants.vala',
    c_args: c_args,
    dependencies: [
        deps
    ],
    install : true
)

subdir('data')