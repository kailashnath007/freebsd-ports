# Created by: Solène RAPENNE <solene@bsd.zplay.eu>
# $FreeBSD$

PORTNAME=	sxiv
PORTVERSION=	1.3.1
PORTREVISION=	1
CATEGORIES=	graphics
MASTER_SITES=	https://github.com/muennich/sxiv/archive/
DISTNAME=	v${PORTVERSION}

MAINTAINER=	solene@bsd.zplay.eu
COMMENT=	Lightweight image viewer

LICENSE=	GPLv2

LIB_DEPENDS=	libImlib2.so:${PORTSDIR}/graphics/imlib2 \
		libexif.so:${PORTSDIR}/graphics/libexif

WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}/
USES=		pkgconfig gmake
USE_XORG=	x11

PLIST_FILES=	bin/sxiv \
		man/man1/sxiv.1.gz \
		share/sxiv/exec/image-info \
		share/sxiv/exec/key-handler

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/sxiv

.include <bsd.port.mk>
