# Created by: Andrew Pantyukhin <infofarmer@FreeBSD.org>
# $FreeBSD$

PORTNAME=	castget
PORTVERSION=	1.0.1
PORTREVISION=	7
CATEGORIES=	www
MASTER_SITES=	SAVANNAH

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Command-line podcast downloader

LICENSE=	LGPL21 # or later
LICENSE_FILE=	${WRKSRC}/COPYING.LIB

LIB_DEPENDS=	libid3.so:${PORTSDIR}/audio/id3lib \
		libcurl.so:${PORTSDIR}/ftp/curl

USE_LDCONFIG=	yes
USES=		libtool pkgconfig
USE_GNOME=	glib20 libxml2
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib
CONFIGURE_ARGS=	--disable-static
GNU_CONFIGURE=	yes
INSTALL_TARGET=	install-strip

PLIST_FILES=	bin/castget include/libcastget.h \
		lib/libcastget.so lib/libcastget.so.0 lib/libcastget.so.0.0.0 \
		man/man1/castget.1.gz man/man5/castgetrc.5.gz

.include <bsd.port.mk>
