# Created by: J.R. Oldroyd <fbsd@opal.com>
# $FreeBSD$

PORTNAME=	xfce4-power-manager
PORTVERSION=	1.4.4
CATEGORIES=	sysutils xfce
MASTER_SITES=	XFCE/src/xfce/${PORTNAME}/${PORTVERSION:R}/
DIST_SUBDIR=	xfce4

MAINTAINER=	xfce@FreeBSD.org
COMMENT=	Power manager for the Xfce Desktop

LICENSE=	GPLv2

LIB_DEPENDS=	libnotify.so:${PORTSDIR}/devel/libnotify \
	libdbus-glib-1.so:${PORTSDIR}/devel/dbus-glib \
	libpolkit-gobject-1.so:${PORTSDIR}/sysutils/polkit \
	libupower-glib.so:${PORTSDIR}/sysutils/upower

GNU_CONFIGURE=	yes
USES=		gettext pkgconfig gmake libtool xfce tar:bzip2
USE_GNOME=	glib20 gtk20 intltool intlhack
USE_XFCE=	panel
INSTALLS_ICONS=	yes
USE_XORG=	xrandr x11 xext xtst xscrnsaver
CONFIGURE_ARGS=	--disable-network-manager \
		--enable-polkit \
		--enable-xfce4panel \
		--disable-lxdepanel

.include <bsd.port.mk>
