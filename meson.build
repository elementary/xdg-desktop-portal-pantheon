project('xdg-desktop-portal-pantheon', 'c', 'vala')

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
libexecdir = join_paths(prefix, get_option('libexecdir'))
localedir = join_paths(prefix, get_option('localedir'))

systemd_dep = dependency('systemd')

glib_dep = dependency('glib-2.0')
gobject_dep = dependency('gobject-2.0')
gio_dep = dependency('gio-2.0')
gtk_dep = dependency('gtk+-3.0')
gdk_dep = dependency('gdk-x11-3.0')
granite_dep = dependency('granite')
handy_dep = dependency('libhandy-1')

add_global_arguments(
    '-DGETTEXT_PACKAGE="@0@"'.format (meson.project_name()),
    language: 'c'
)

conf_data = configuration_data()
conf_data.set('LIBEXECDIR', libexecdir)
conf_data.set_quoted('GETTEXT_PACKAGE', meson.project_name())
conf_data.set_quoted('LOCALEDIR', localedir)

subdir('data')
subdir('src')
