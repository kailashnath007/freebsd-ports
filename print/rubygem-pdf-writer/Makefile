# $FreeBSD$

PORTNAME=	pdf-writer
PORTVERSION=	1.1.8
CATEGORIES=	print rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Pure Ruby PDF document creation library

LICENSE=	MIT

RUN_DEPENDS=	rubygem-color>=1.4.0:${PORTSDIR}/print/rubygem-color \
		rubygem-transaction-simple>=1.3:${PORTSDIR}/devel/rubygem-transaction-simple

USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

PLIST_FILES=	bin/techbook

.include <bsd.port.mk>
