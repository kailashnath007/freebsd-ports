# Created by: bsam
# $FreeBSD$

PORTNAME=	ungif
PORTVERSION=	4.1.3
CATEGORIES=	graphics linux
MASTER_SITES=	LOCAL/ehaupt/rpm/${LINUX_RPM_ARCH}/fedora/${LINUX_DIST_VER}
DISTNAME=	${LINUX_NAME}-${PORTVERSION}-${RPMVERSION}

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	RPM of gif and ungif libs (Linux Fedora 10)

CONFLICTS=	linux-ungif-[0-9]* linux-f8-ungif-[0-9]*

ONLY_FOR_ARCHS=	i386 amd64
USE_LINUX=	f10
USE_LINUX_RPM=	yes
LINUX_NAME=	giflib

RPMVERSION=	9
USE_LDCONFIG=	yes

PLIST_FILES=	usr/lib/libgif.so.4 \
		usr/lib/libgif.so.${PORTVERSION} \
		usr/lib/libungif.so.4 \
		usr/lib/libungif.so.${PORTVERSION}
DOCSDIR=	${PREFIX}/usr/share/doc/giflib-${PORTVERSION}
PORTDOCS=	AUTHORS BUGS COPYING ChangeLog NEWS ONEWS README TODO

.include <bsd.port.mk>
